# DOMcalculator.github.io
<!DOCTYPE html>
<html>
<head>
<title>Calculator</title>
<script>

function insert(num)
{
   document.form1.textview.value = document.form1.textview.value + num;
}

function equal()
{
   var exp = document.form1.textview.value;
   if(exp)
   {
      document.form1.textview.value = eval(exp)
   }
}
function backspace()
{
   var exp = document.form1.textview.value;
   document.form1.textview.value = exp.substring(0, exp.length - 1);
 
}
</script>
<style>

.formstyle
{
   width: 300px;
   height: 330px;
   margin: 20px auto;
   border: 3px solid black;
   border-radius: 5px;
   padding: 20px;
   text-align: center;
   background-color: grey;
}

h1 {
   text-align: center;
   padding: 23px;
   
   color: black;
   }
input:hover
{
   background-color: green;
}  
*{
   margin: 0;
   padding: 0;
}

.btn{
   width: 50px;
   height: 50px;
   font-size: 25px;
   margin: 2px;
   cursor: pointer;
   background-color: lightgray;
   color: white;
}


.textview{
   width: 223px;
   margin: 5px;
   font-size: 25px;
   padding: 5px;
   background-color: lightgreen;
}    
</style>
</head>
<body>
<h1>CALCULATOR</h1>
 <div class= "formstyle">
 <form name = "form1">
 <input class= "textview" name = "textview">
 </form>
 <center>
 <table >
 <tr>
   <td> <input class = "btn" type = "button" value = "C" onmouseout= "form1.textview.value = ' ' " > </td>
   <td> <input  class = "btn" type = "button" value = "B" onclick = "backspace()" > </td>
   <td> <input  class = "btn" type = "button" value = "/" onclick = "insert('/')" > </td>
   <td> <input class = "btn" type = "button" value = "x" onclick = "insert('*')" > </td>
   </tr>
   
   <tr>
   <td> <input class = "btn" type = "button" value = "7" onclick = "insert(7)" > </td>
   <td> <input class = "btn" type = "button" value = "8" onclick = "insert(8)" > </td>
   <td> <input class = "btn" type = "button" value = "9" onclick = "insert(9)" > </td>
   <td> <input class = "btn" type = "button" value = "-" onclick = "insert('-')" > </td>
   </tr>
   
   <tr>
   <td> <input class = "btn" type = "button" value = "4" onclick = "insert(4)" > </td>
   <td> <input class = "btn" type = "button" value = "5" onclick = "insert(5)" > </td>
   <td> <input class = "btn" type = "button" value = "6" onclick = "insert(6)" > </td>
   <td> <input class = "btn" type = "button" value = "+" onclick = "insert('+')" > </td>
   </tr>
   
   <tr>
   <td> <input class = "btn" type = "button" value = "1" onclick = "insert(1)" > </td>
   <td> <input class = "btn" type = "button" value = "2" onclick = "insert(2)" > </td>
   <td> <input class = "btn" type = "button" value = "3" onclick = "insert(3)" > </td>
   <td rowspan = 5> <input class = "btn" style = "height: 110px" type = "button" value = "=" onmouseover= "equal()"> </td>
   </tr>
   <tr>
   <td colspan = 2> <input class = "btn" style = "width: 106px" type = "button" value = "0" onclick = "insert(0)" > </td>
   <td> <input class = "btn" type = "button" value = "." onclick = "insert('.')"> </td>
   </tr>
   </table>
   </center>
</div>
</body>
</html>
