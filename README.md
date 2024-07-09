# CodSoft
Calculator Using HTML & CSS
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="task3style.css">
</head>
<body>
    <div class="box">
        <div class="calc">
            <form>
                <div class="result">
                    <input type="text" name="result">
                </div>
                <div>
                    <input type="button" value="AC" onclick="result.value = '' ">
                    <input type="button" value="DE" onclick="result.value = result.value.toString().slice(0,-1) ">
                    <input type="button" value="." onclick="result.value += '.' ">
                    <input type="button" value="/" onclick="result.value += '/' ">
                </div>
                <div>
                    <input type="button" value="7" onclick="result.value += '7' ">
                    <input type="button" value="8" onclick="result.value += '8' ">
                    <input type="button" value="9" onclick="result.value += '9' ">
                    <input type="button" value="*" onclick="result.value += '*' ">
                </div>
                <div>
                    <input type="button" value="4" onclick="result.value += '4' ">
                    <input type="button" value="5" onclick="result.value += '5' ">
                    <input type="button" value="6" onclick="result.value += '6' ">
                    <input type="button" value="-" onclick="result.value += '-' ">
                </div>
                <div>
                    <input type="button" value="1" onclick="result.value += '1' ">
                    <input type="button" value="2" onclick="result.value += '2' ">
                    <input type="button" value="3" onclick="result.value += '3' ">
                    <input type="button" value="+" onclick="result.value += '+' ">
                </div>
                <div> 
                    <input type="button" value="00" onclick="result.value += '00' ">
                    <input type="button" value="0" onclick="result.value += '0' ">
                    <input type="button" value="=" class="ans" onclick="result.value = eval(result.value)">
                </div>
            </form>
        </div>
    </div>
</body>
</html>

!-- CSS CODE --!

*{
    margin: 0;
    padding: 0;
    font-family: 'poppins',sans-serif;
    box-sizing: border-box;
}
.box{
    width: 100%;
    height: 100vh;
    background-color: white;
    display: flex;
    align-items: center;
    justify-content: center;
}
.calc{
    background-color:rgb(0, 139, 139);
    padding: 20px;
    border-radius: 10px;
}
.calc form input{
    border: 1px;
    outline: 0;
    width: 60px;
    height: 60px;
    border-radius: 12px;
    box-shadow: -8px -8px 15px rgba(255,255,255,0.1),5px 5px 15px rgba(0,0,0,0.2);
    background: transparent;
    font-size: 20px;
    color:white;
    background-color: rgb(0, 131, 131);
    cursor: pointer;
    margin: 10px;
}
form .result{
    display: flex;
    justify-content: flex-end;
    margin: 20px 0;
}
form .result input{
    text-align: right;
    flex: 1;
    font-size: 45px;
    box-shadow: none;
}
form input.ans{
    width: 140px;
}
