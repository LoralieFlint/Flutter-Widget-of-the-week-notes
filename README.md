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
similar to accessibility in web side with images and links with alt tags 
use Tooltip for screen readers

Tooltip(
    message: 'Dash',
    verticalOffset: 40,
    height: 24,
    child: MyVisualWidget(),
)

#### some Material widgets already come with Tooltip included such as IconButton
IconButton(
    iconButton: Icon(Icons.high.quality),
    tooltip: 'high quality',
)


# FiitedBox
this works very similar to flexbox in CSS 

MyBlueRect(
    child: FittedBox(
        alignment: Alignment.centerLeft,
        fit: BoxFit.contain,
        child: MyCatPic(),
    ),
)

# LayoutBuilder
the builder function has built in parameter for incoming box constraints so knowing the valid width and height constraints for our device is at ease

Widget build(BuildContext context) {
    return LayoutBuilder(
        builder: (context, constraints) {
            if(constraints.maxWidth < 600) {
                return MyOneColumnLayout();
            }else{
                return MyTwoColumnLayout();
            }
        },
    );
}