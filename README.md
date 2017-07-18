# Canvas
HTML5 Canvas Self-study summary

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Learning the basics of canvas</title>
    <link rel="stylesheet" href="">
    <script type="text/javascript" src="http://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
    <!-- <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script> -->

    <script type="text/javascript">
        $(document).ready(function() {
            var canvas = $("#myCanvas");
            var context = canvas.get(0).getContext("2d");
            //绘制填充矩形
            context.fillRect(40,40,100,100);//绘制一个从原点(40,40)宽100，高100的图形并填充
            //context.fillRect(x,y,width,height);
            
            //绘制矩形轮廓
            context.strokeRect(150,40,100,100);//绘制一个矩形轮廓
            //context.strokeRect(x,y,width,height);
            
            //绘制线条
            context.beginPath();//开始路径
            context.moveTo(260,40);//设置路径原点
            context.lineTo(360,40);//继续连接
            context.lineTo(360,140);//设置路径终点
            context.closePath();//结束路径
            context.fill();//填充路径闭合的图形
            // context.stroke();//绘出路径轮廓
        });
    </script>
    
</head>
<body>
    <canvas id="myCanvas" width="500" height="500">
        <!-- 你的浏览器不支持canvas，请升级-->
    </canvas>
</body>
</html>
