<!DOCTYPE html>
<html>
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
form { 
  display: block;
  margin-left: 15px;
}
body{
background-color:orange;
}
</style>
</head>
<body>



<form action="home.html" method="get">
	<table>
<tr>
    <td>User name</td>
    <td><input type="text" placeholder="username"></td>
</tr>
<tr>
    <td>password</td>
   	<td><input type="password" id="password" placeholder="password"></td>
</tr>
<tr>
    <td>confirm_password</td>
   	<td><input type="password" id="confirm_password" placeholder="Retype password"></td>
</tr>

<tr>
	<td>
	<input class="style" type="submit" onclick="validatePassword()" value="Submit">
	</td>
</tr>

	</table>


</form>
<script>
var password = document.getElementById("password")
, confirm_password = document.getElementById("confirm_password");

function validatePassword(){
if(password.value != confirm_password.value) {
  confirm_password.setCustomValidity("Passwords not matchning");
} else {
  confirm_password.setCustomValidity('');
}
}

password.onchange = validatePassword;
confirm_password.onkeyup = validatePassword;
</script>
</body>
</html>
