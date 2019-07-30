## 设置网页打开加密或JS网页加密通过js混淆代码加密代码
<script>
function password() {
var testV = 3;
var pass1 = prompt('请输入查看密码!','');
while (testV < 1) {
if (!pass1)
history.go(0);
if (pass1 == "设置密码") {
break;
}
testV+=1;
var pass1 =
prompt('密码错误!');
}
if (pass1!="设置密码" & testV ==3)
history.go(0);
return " ";
}
document.write(password());
</script>

## 其他