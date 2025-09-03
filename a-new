<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>A-mine</title>
    <style>
        body {
            background: linear-gradient(45deg, #6ee5e9, #4088da, #171ac7, #400a97, #961dce, #e42172);
            background-size: 400% 400%;
            animation: gradientShift 8s ease infinite;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        th, td {
            border-collapse: collapse;
            margin-top: 50px;
            width: 100px;
            height: 100px;
        }
        p {
            display: none;
            font-size: 50px;
            text-align: center;
            margin-top: -10px;
            margin-bottom: -10px;
        }
        table {
            margin: 50px auto;
            border-collapse: separate;
            border-spacing: 3px;
        }
        td {
            position: relative;
        }
        td:nth-child(1), td:nth-child(2), td:nth-child(3) {
            border-right: 5px solid #333;
        }
        td:nth-child(3) {
            border-right: none;
        }
        tr:nth-child(1) td, tr:nth-child(2) td {
            border-bottom: 5px solid #333;
        }
        tr:nth-child(3) td {
            border-bottom: none;
        }
        #y, #c {
            background-color: #000;
            color: #fff;
            width: 100px;
            height: 50px;
            font-size: 20px;
        }
        button {
            background: none;
            border: none;
            width: 100px;
            height: 100px;
            font-size: 50px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h2>who's got the 1st turn?</h2>
    <button id="y" onclick="alert('go ahead')">you</button> <button id="c" onclick="firstplayer()">computer</button>
    <table>
        <tr>
            <td><button onclick="corner1()" id="00"></button><p id="X00">X</p><p id="O00">O</p></td>
            <td><button onclick="edge1()" id="01"></button><p id="X01">X</p><p id="O01">O</p></td>
            <td><button onclick="corner2()" id="02"></button><p id="X02">X</p><p id="O02">O</p></td>
        </tr>
        <tr>
            <td><button onclick="edge2()" id="10"></button><p id="X10">X</p><p id="O10">O</p></td> 
            <td><button onclick="center()" id="11"></button><p id="X11">X</p><p id="O11">O</p></td> 
            <td><button onclick="edge3()" id="12"></button><p id="X12">X</p><p id="O12">O</p></td> 
        </tr>
        <tr> 
            <td><button onclick="corner3()" id="20"></button><p id="X20">X</p><p id="O20">O</p></td>
            <td><button onclick="edge4()" id="21"></button><p id="X21">X</p><p id="O21">O</p></td> 
            <td><button onclick="corner4()" id="22"></button><p id="X22">X</p><p id="O22">O</p></td> 
        </tr>
    </table>
    <script>
        let count = 0;
        let first = false;
        let victory = false;
        let edge1x = false;
        let edge2x = false;
        let edge3x = false;
        let edge4x = false;
        let corner1x = false;
        let corner2x = false;
        let corner3x = false;
        let corner4x = false;
        let centerx = false;
        let edge1o = false;
        let edge2o = false;
        let edge3o = false;
        let edge4o = false;
        let corner1o = false;
        let corner2o = false;
        let corner3o = false;
        let corner4o = false;
        let centero = false;
        function corner1() {
            document.getElementById("00").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X00").style.display="block";
                corner1x = true;
            } else {
                document.getElementById("O00").style.display="block";
                corner1o = true;
            }
            Victory();
        }
        function edge1() {
            document.getElementById("01").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X01").style.display="block";
                edge1x = true;
            } else {
                document.getElementById("O01").style.display="block";
                edge1o = true;
            }
            Victory();
        }
        function corner2() {
            document.getElementById("02").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X02").style.display="block";
                corner2x = true;
            } else {
                document.getElementById("O02").style.display="block";
                corner2o = true;
            }
            Victory();
        }
        function edge2() {
            document.getElementById("10").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X10").style.display="block";
                edge2x = true;
            } else {
                document.getElementById("O10").style.display="block";
                edge2o = true;
            }
            Victory();
        }
        function center() {
            document.getElementById("11").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X11").style.display="block";
                centerx = true;
            } else {
                document.getElementById("O11").style.display="block";
                centero = true;
            }
            Victory();
        }
        function edge3() {
            document.getElementById("12").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X12").style.display="block";
                edge3x = true;
            } else {
                document.getElementById("O12").style.display="block";
                edge3o = true;
            }
            Victory();
        }
        function corner3() {
            document.getElementById("20").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X20").style.display="block";
                corner3x = true;
            } else {
                document.getElementById("O20").style.display="block";
                corner3o = true;
            }
            Victory();
        }
        function edge4() {
            document.getElementById("21").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X21").style.display="block";
                edge4x = true;
            } else {
                document.getElementById("O21").style.display="block";
                edge4o = true;
            }
            Victory();
        }
        function corner4() {
            document.getElementById("22").style.display="none";
            count++;
            if(count%2==0){
                document.getElementById("X22").style.display="block";
                corner4x = true;
            } else {
                document.getElementById("O22").style.display="block";
                corner4o = true;
            }
            Victory();
        }
        function firstplayer() {
            first = true;
            randomechoice();
        }
        function randomechoice() {
        let choices = [corner1, edge1, corner2, edge2, center, edge3, corner3, edge4, corner4];
        choices = choices.filter(fn => {
            if (fn === corner1) return !corner1x && !corner1o;
            if (fn === edge1)   return !edge1x   && !edge1o;
            if (fn === corner2) return !corner2x && !corner2o;
            if (fn === edge2)   return !edge2x   && !edge2o;
            if (fn === center)  return !centerx  && !centero;
            if (fn === edge3)   return !edge3x   && !edge3o;
            if (fn === corner3) return !corner3x && !corner3o;
            if (fn === edge4)   return !edge4x   && !edge4o;
            if (fn === corner4) return !corner4x && !corner4o;
        });
        let randomIndex = Math.floor(Math.random() * choices.length);
        let randomFunc = choices[randomIndex];
        randomFunc();
        }
        function Victory() {
            if(corner1x&&edge1x&&corner2x||corner3x&&edge4x&&corner4x||edge2x&&centerx&&edge3x||corner1x&&edge2x&&corner3x||corner2x&&edge3x&&corner4x||edge1x&&centerx&&edge4x||corner1x&&centerx&&corner4x||corner2x&&centerx&&corner3x){
                alert("X is the winner");
                victory = true;
                location.reload();
            } else if(corner1o&&edge1o&&corner2o||corner3o&&edge4o&&corner4o||edge2o&&centero&&edge3o||corner1o&&edge2o&&corner3o||corner2o&&edge3o&&corner4o||edge1o&&centero&&edge4o||corner1o&&centero&&corner4o||corner2o&&centero&&corner3o){
                alert("O is the winner");
                victory = true;
                location.reload();
            }else if(count==9){
                alert("it's a tie");
                location.reload();
            }
            if(first&&count%2==0){
                randomechoice();
            }
            if(!first&&count%2==1){
                randomechoice();
            }
        }
    </script>
</body>
</html>
