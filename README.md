# Simple Interest Calculator

This is a simple interest calculator that takes the principal amount, time period in years, and the annual rate of interest as input and calculates the simple interest.

## HTML Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Interest Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input[type="number"] {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #28a745;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #218838;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Simple Interest Calculator</h2>
        <form id="interestForm">
            <label for="principal">Principal Amount (P):</label>
            <input type="number" id="principal" name="principal" required>

            <label for="time">Time Period (T) in years:</label>
            <input type="number" id="time" name="time" required>

            <label for="rate">Annual Rate of Interest (R) %:</label>
            <input type="number" id="rate" name="rate" step="0.01" required>

            <button type="button" onclick="calculateInterest()">Calculate Interest</button>
        </form>
        <div class="result" id="result"></div>
    </div>

    <script>
        function calculateInterest() {
            var p = document.getElementById('principal').value;
            var t = document.getElementById('time').value;
            var r = document.getElementById('rate').value;

            if (p && t && r) {
                var interest = (p * t * r) / 100;
                document.getElementById('result').innerHTML = 'Simple Interest: ' + interest;
            } else {
                document.getElementById('result').innerHTML = 'Please fill in all fields.';
            }
        }
    </script>
</body>
</html>

