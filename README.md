# CustomPaint
uses 2 methods 
1. paint -- this is where you get your canvas and you are free to draw.
2. shouldRepaint -- this is called when the custom painter is rebuilt.

CustonPaint(
    size: Size(200.0),
    painter: MyPainter(),
)

class MyPainter extends CustomPaint{
    @override
    void paint( Canvas canvas, Size size,) {
        // .....
    }

 @override
    bool shouldRepaint( Custompaint old) {
        // .....
    }
}

##### paint whatever you want!
canvas.drawLine() 
canvas.drawRect() 
canvas.drawCircle() 
canvas.drawArc() 
canvas.drawPath() 
canvas.drawImage() 
canvas.drawImageNine() 
canvas.drawParagraph() 

##### paint however you want!
colors, shaders, blend modes, etc.

# Tooltip
