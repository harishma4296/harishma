<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8"/>
    <title>Stock Trading Application</title>
    <style>
        table {
            border: 1px solid black;
            border-collapse: collapse;
            width: 20%;
        }
        td {
            border: 1px solid black;
            border-collapse: collapse;
            text-transform: uppercase;
        }
        th {
            font-weight: bold;
            border: 1px solid black;
            border-collapse: collapse;
            text-transform: uppercase;
        } 
    </style>
    <script>
        function validateStock() {
            var quantity = document.forms['stock']['qty'].value;
            quantity = parseInt(quantity);
            if(quantity < 10 || quantity > 100 || quantity % 10 !== 0)
                alert("INVALID QUANTITY");
        }
    </script>
</head>
<body style="margin: 0.5in;">
<div>
    <table id="table">
        <tr>
            <th>ticker</th>
            <th>price</th>
        </tr>
        <tr>
            <td>wipro</td>
            <td>298.45</td>
        </tr>
        <tr>
            <td>infy</td>
            <td>949.95</td>
        </tr>
        <tr>
            <td>tcs</td>
            <td>2713.70</td>
        </tr>
        <tr>
            <td>techm</td>
            <td>485.85</td>
        </tr>
    </table>
</div>
<div>
    <form name="stock" onsubmit="validateStock()">
        <h1>Stock Trading</h1>
        <table style="border: 0;">
            <tr>
                <td style="border: 0;  text-transform: capitalize;">ticker:</td>
                <td style="border: 0; text-transform: uppercase;"><input type="text" name="ticker"></input></td>
            </tr>
            <tr>
                <td style="border: 0;  text-transform: capitalize;">qantity:</td>
                <td style="border: 0;"><input type="text" name="qty"></input></td>
            </tr>
            <tr style="height: 12pt;"></tr>
            <tr>
                <td style="border: 0;"></td>
                <td style="border: 0;"><input type="submit" name="submit" value="Submit"></td>
            </tr>
        </table>
    </form>
</div>
<div id='debug'></div>
</body>
</html>
