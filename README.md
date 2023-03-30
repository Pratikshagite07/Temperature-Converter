# Temperature-Converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Conversion </title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="container">
        <div class="input_box">
            <label for="celsius">Celsius</label>
            <input type="number" id="celsius" oninput="celToFar()" placeholder="value">
        </div>
        <div class="input_box">
            <label for="fahrenheit">Fahrenheit</label>
            <input type="number" id="fahrenheit" oninput="farToCel()" placeholder="value">
        </div>
    </div>
    <script src="script.js"></script>

</body>

</html>
 let celsius = document.getElementById("celsius");
let fahrenheit = document.getElementById("fahrenheit");

function celToFar() {
    let output = (parseFloat(celsius.value) * 9 / 5) + 32;
    fahrenheit.value = parseFloat(output.toFixed(2));
}

function farToCel() {
    let output = (parseFloat(fahrenheit.value) - 32) * 5 / 9;
    celsius.value = parseFloat(output.toFixed(2));
    console.log(output);
}
@import url('https://fonts.googleapis.com/css2?family=Baloo+2&display=swap');
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Pattaya', sans-serif;
}

body {
    background-color: #131212;
}

.container {
    width: 450px;
    background-color: #f8cb76;
    padding: 70px 40px;
    position: absolute;
    transform: translate(-50%, -50%);
    left: 50%;
    top: 50%;
    box-shadow: 0 20px 25px rgba(226, 156, 63, 0.25);
    border-radius: 8px;
    font-size: 18px;
}

.input_box {
    width: 51%;
    margin-left: 95px;
    margin-bottom: 42px;
}

label {
    font-size: 30px;
    font-weight: 600;
    border: 2px dashed #e66d6d;
    border-radius: 3px;
}

input {
    width: 100%;
    height: 50px;
    border-radius: 9px;
    border: 2px solid #1e0d0d;
    outline: none;
    margin-top: 8px;
    padding: 0 10px;
}

input:focus {
    border: 2px dashed #f35d5d;
    background-color: #d4ccdd;
}
        
