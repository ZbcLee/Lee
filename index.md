<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .box1{
            width: 800px;
            height: 600px;
            background-color: black;
            position: relative;
            top: calc(10vw + 100px);
            margin: auto;
        }
        .box2,
        .box3 {
            width: 180px;
            height: 288px;
            background-color: red;
            position: absolute;
            top: 50%;
            bottom: 50%;
            text-align:center;
            margin: auto;
            border-radius: 120px/145px;
            border-bottom-left-radius: 0%;
            border-bottom-right-radius: 0%;
            /* transform-origin: 300px 400px; */
        }        
        span{
            vertical-align: middle;
            line-height: 200px;
        }
        .box2{
            left:0px;
            border-bottom-left-radius: 15px;
            border-bottom-right-radius: 15px;
            animation: move1 1s linear forwards, move2 3s linear forwards, move5 1s ease-in alternate infinite 3s;
        }
        .box3{
            right: 0px;
            border-bottom-left-radius: 15px;
            border-bottom-right-radius: 15px;
            animation: move3 1s linear forwards, move4 1s linear forwards,move6 1s ease-in alternate infinite 3s;
        } 

        @keyframes move1{
            from{transform: translate(0px, 0px)}
            to {transform: translate(271.2px, 0px)}
        }
        @keyframes move2{
            from{transform: translate(271.2px, 0px) rotate(0deg)}
            to {transform: translate(271.2px, 0px) rotate(-45deg)}
        }

        @keyframes move3{
            from{transform: translate(0px, 0px)}
            to {transform: translate(-271.2px, 0px)}
        }
        @keyframes move4{
            from{transform: translate(-271.2px, 0px) rotate(0deg)}
            to {transform: translate(-271.2px, 0px) rotate(45deg)}
        }
        @keyframes move5{
            from{transform: translate(271.2px, 0px) rotate(-45deg) scale(0.95)}
            to {transform: translate(271.2px, 0px) rotate(-45deg) scale(1.05)}
        }
        @keyframes move6{
            from{transform: translate(-271.2px, 0px) rotate(45deg) scale(0.95)}
            to {transform: translate(-271.2px, 0px) rotate(45deg) scale(1.05)}
        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="box2"></div>
        <div class="box3"></div>
    </div>
</body>
</html>
