<html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>Add More Qualification</title>
<style>
form{
margin: 20px 0;
}
form input, button{
padding: 5px;
}
table{
width: 100%;
margin-bottom: 20px;
border-collapse: collapse;
}
table, th, td{
border: 1px solid #cdcdcd;
}
table th, table td{
padding: 10px;
text-align: left;
}
</style>
<script src="https://code.jquery.com/jquery-1.12.4.min.js"></script>
<script>
$(document).ready(function(){
$(".add-row").click(function(){
var name = $("#name").val();
var examname = $("#examname").val();
var grade = $("#grade").val();
var year = $("#year").val();
var markup = "<tr><td><input type='checkbox' name='record'></td><td>" + name + "</td><td>" + examname + "</td> <td>" + grade + "</td> <td>" + year+"</td></tr>";
$("table tbody").append(markup);
});

// Find and remove selected table rows
$(".delete-row").click(function(){
$("table tbody").find('input[name="record"]').each(function(){
if($(this).is(":checked")){
$(this).parents("tr").remove();
}
});
});
});    
</script>
</head>
<body>
<center><h1> Add Educational Background </h1> </center>
<form>
<input type="text" id="name" placeholder="Name"><br><p></p>
<input type="text" id="examname" placeholder="Exam Name">
<input type="text" id="grade" placeholder="Grade/GPA">
<input type="text" id="year" placeholder="Year">
<input type="button" class="add-row" value="Add Row">
</form>
<table>
<thead>
<tr>
<th>Select</th>
<th>Your Name</th>
<th>Exam Name</th>
<th>Grade/GPA</th>
<th>Year</th>
</tr>
</thead>
<tbody>
<!-- <tr>
<td><input type="checkbox" name="record"></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr> -->
</tbody>
</table>
<button type="button" class="delete-row">Delete</button>
</body> 
</html>                            
