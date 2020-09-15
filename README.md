# Simple-calculator

<!DOCTYPE html>
<html>
<head>
	<title>Simple calculator</title>
	<style type="text/css">
		table, th, td {
			background: DarkBlue;
			BORDER=2px Black;
			width=100%
		}
		button{
			width: 100%;
		}
	</style>
	<script type="text/javascript">
		function calc(clicked_id)
		{
			var a=parseFloat(document.getElementById('v1').value);
			var b=parseFloat(document.getElementById('v2').value);
			if(clicked_id=='clr')
			{
				v1.value="";
				v2.value="";
				r.value="";
			}
			else if(isNaN(a)|isNaN(b))
			{
				window.alert("Enter The Valid Number!!!");
			}
			else
			{
				if(clicked_id=='a')
					document.getElementById('r').value=a+b;
				if(clicked_id=='s')
					document.getElementById('r').value=a-b;
				if(clicked_id=='m')
					document.getElementById('r').value=a*b;
				if(clicked_id=='d')
					document.getElementById('r').value=a/b;
			}
		}
	</script>
</head>
<body bgcolor=gray text=white>
	<center>
	<table>
		<tr><th colspan="4"><b>Simple Calculator</b></th></tr>
		<tr><th>First Value </th><td><input type="text" placeholder="Enter the First value" id="v1"></td>
			<th>Second Value </th><td><input type="text" placeholder="Enter the Second value" id="v2"></td></tr>
		<tr><td><button onclick="calc(this.id)" id='a'>Addition</button></td>
			<td><button onclick="calc(this.id)" id='s'>Subtraction</button></td>
			<td><button onclick="calc(this.id)" id='m'>Multiplication</button></td>
			<td><button onclick="calc(this.id)" id='d'>Division</button></td></tr>
		<tr><th colspan="2">Result</th><td colspan="2"><input type="text" placeholder="Waiting for Result" id="r"></td></tr>
		<tr><td colspan="4"><button onclick="calc(this.id)" id='clr'>Clear</button></td></tr>
	</table>
	</center>
</body>
</html>
