## 第一节课：类与对象的概念
```php
    1 、想造N个人的对象
    需要先：创建人类，且只需要创建1次
    然后再：由类创造人的对象，可以N次

    2、 如何声明类
    对象有什么？  属性（身高，体重，姓名）
    对象能干什么？功能（哭，笑，招呼，吃饭）
    思考：用‘变量’和‘函数’来模拟‘属性’和‘功能’

    我们把{N个属性+N个方法}打包成一个‘东西’
    其实就是N个变量，N个函数，打包到某个对象里
    这个对象可以使用N个变量，N个函数,这个就是对象

    3、声明语法：
    class 类名{
        属性+方法
    }

    //创建一个人的类
    class People{
        public $name = 'nobody';
        public $height = '30cm';
        public function cry(){
            echo '呱呱坠地'
        }
    }

    //有了类，就可以产生对象
    new类名（）；这个语句返回对象
    print_r(new People());//打印对象函数

    //返回的对象需要永久保存 赋值给一个变量
    $a = new People();
    $a是一个复合/关联数组，里面包含属性和属性值

    //如何访问对象里的属性值
    $a->name  //输出：echo $a->name;

    //类对比复合/关联数组 结果一样
    $b = array('name'=>'nobodyB','height'=>'40B');
    echo $b['name'],'<br />',$b['height'];

    //但是对象比数组高级 对象能调用方法，方法就是函数，属性就是变量。
    $a->cry(); //调用类的方法
```

## 第二节课：属性与方法的注意点
```php
    再从程序的角度、数据的角度深入分析类与对象
    声明类时的注意事项：
        [重要]创建对象时，有哪些操作？

    一：属性值：
        ①可以声明属性并赋值，也可以声明属性先不赋值
        如果不赋值，则属性的初始值为：NULL

        class Human{
            public $age = 0;
        }
        class People{
            public $age;
        }
        $b = new People();
        //echo 无法打印出NULL.必须用var_dump();
        echo $b->age,'<br />';
        var_dump($b->age,'<br />');

        ②：关于PHP中的类，请注意：属性必须是一个“直接的值”.
        是8中类型任意的“值”.
        不能是 表达式  如1+2的值；
        不能是 函数的返回值 如time()

        注意：这点和java不一样 java可以

        class Human{
            //public $age = 1+2; //php中错误，java中正确
            //public $age = time(); //php中错误，java中正确
            public $age = 1;            
        }

    二：方法注意点：
        ①：PHP中函数不能重复定义（定义重复）
            这点和js不一样，JS中是可以重复定义的
            系统函数不能定义，如:time（）是系统函数，不能重复定义
        
        ②:类中的方法,可以理解包在类范围内的函数和全局的函数，因此可以与外部重名.
        
            类内部函数和外部函数或系统函数。
            ->想调用内部函数必须加$this->函数名
            ->想调用外部函数或系统函数不加$this调用。

        例：
        class Clock{
            public function time(){
                echo '现在的时间戳是2019年6月';
            }
            public function t(){
                return '调用内部的函数t';
            }
            public function time(){
                //注意此处调用的是系统的time()函数
                echo '现在真正的时间戳是',<br />;
                //注意此处调用的是自身的t（）函数；
                echo $this->t(); 
            }
        }
        $c = new Clock();
        $c->time();
        echo '<br />';
        $c->time2();
```

## 第三节课：构造函数详解
```php
    重点：
        构造函数与析构函数  __construct();两个下划线
        构造函数的作用时机：
        每当new一个对象，就会自动新new出来的对象发挥作用
        构造函数即构造方法
        new ClassName($args);
        $args参数原样传给构造方法；

        当然new ClassName($args)也可以不传参数
        但要注意 $args要与构造方法里的参数一致。对应位置

    1、构造函数 __construct()

        例子：
        class Human{
            public $name = '李四';
            public $gender = '男';
        }
        $a = new Human();
        $b = new Human();
        $c = new Human();
        echo $a->name;
        echo $b->name;
        echo $c->name;
        echo $a->gender;
        echo $b->gender;
        echo $c->gender;
        以上的例子中，体现出类时模板，对象根据模板造出实例
        但是，模板是固定的。

        因此，导致造出来的对象，各种属性值都一样
        这显然与现实生活中的逻辑不符合。

        比如：新生儿 性别  姓名 体重 这些都不一样
        同一个模板，不同的对象 这就是一对矛盾？ 

        想一想：为什么新生儿有的男，有的女？
        答：因为，染色体不一样
        x,y ->男性
        x,x ->女性
        造对象时，传X染色体，还是y染色体，都有可能
        这就说明创建对象时，可以传 参数

        在类中，有一个构造函数，
        就是用来初始化对象用，
        利用构造函数，你有机会操作对象，
        并改变他的值
        例子：
        class Human{
            public function __construct（）{ 
                echo '紫薇星下凡了';           
            }
            public $name = null;
            public $gender = null;
        }
        $a = new Human();
        
    2、构造函数（即：构造方法）的传参，并影响对象
        //先按类的声明把属性凑齐了  再用__construnct去影响
        //再返回该对象 这就是对象与构造函数的关系
        class Human{
            public function __construct（$name,$gender）{ 
                $this->name = $name;
                $this->gender = $gender； 
            }
            public $name = null;
            public $gender = null;
        }
        $a = new Human('张飞'，'男');
        echo $a->name;//输出张飞
        
```

## 第四节课：
```php
```

## 第五节课：
```php
```
