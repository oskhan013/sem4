## PRACTICAL  1
#### AIM: To Draw the following shapes on the Screen
```

//Line
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
line(100,200,300,300);
getch();
closegraph(); 
}

//Circle

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
circle(200,200,50);
getch();
closegraph();
} 

//	Arc

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
arc(200,200,0,90,50);
getch();
closegraph();
}

```

## PRACTICAL  2

#### AIM: To Draw the following shapes on the Screen

```
//	Bar

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");                  
bar(100,100,300,300);
getch();
closegraph(); 
}

//	3Dbar
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
bar3d(100,100,300,300,20,1);
getch();
closegraph();
}
 
//	Rectangle

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
rectangle(100,100,300,300);
getch();
closegraph(); 
}

```

## PRACTICAL  3

#### AIM: To Draw the following shapes on the Screen

```
//	Ellipse + fillellipse

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
ellipse(200,200,0,360,50,25);
fillellipse(100,100,50,25)
getch(); 
closegraph();
}

//	Drawpoly+ fillpoly

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
int poly1[]={300,150,400,300,250,300,300,150};
int poly2[]={450,150,550,300,400,300,450,150};
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
drawpoly(4,poly1);
fillpoly(4,poly2);
getch(); 
closegraph();
}
```
## PRACTICAL 4

#### AIM: To Draw the Hut on the screen
```

#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
rectangle (150,180,250,300);
rectangle (250, 180,420,300);
rectangle (180,250,220,300);
line(200, 100, 150, 180);
line (200,100,250,180); 
line (200, 100,370,100);
line (370, 100, 120, 180); 
getch();
closegraph();
}
```
## PRACTICAL 5[A]

#### AIM: To Divide computer screen into four regions.
```

#include<stdio.h>
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm;
int xcen,ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen= getmaxx()/2;
ycen=getmaxy()/2;
line(xcen,0,xcen,getmaxy()); 
line(0,ycen, getmaxx(),ycen);
getch();
closegraph();
}
```
## PRACTICAL 5[B]
#### AIM: To Draw circle, rectangle, ellipse, half ellipse into the four regions.
```

#include <graphics.h>
#include <conio.h>
void main() {
int gd = DETECT, gm;
int xcen, ycen;
initgraph(&gd, &gm, "C:\\TURBOC3\\BGI");
xcen = getmaxx() / 2;
ycen = getmaxy() / 2;
line(xcen, 0, xcen, getmaxy());
line(0, ycen, getmaxx(), ycen);
circle(xcen+(-150),ycen-(120),40);
rectangle(xcen + 100, ycen - 100, xcen + 200, ycen - 150);
ellipse(xcen+(-150), ycen-(-100), 0, 360,xcen+(-250),ycen-(200));
ellipse(xcen + xcen / 2, ycen + ycen / 2, 0, 180, 100, 50);
getch();
closegraph();
} 
```
## Practical 6

#### AIM: Draw the following basic shapes in the center of the screen
```

// ❖Circle, ❖ Rectangle, ❖ Square, ❖ Ellipse, ❖Line

#include<graphics.h>
#include<conio.h>
void main() {
int gd=DETECT,gm;
int xcen, ycen;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
xcen=getmaxx()/2;
ycen=getmaxy()/2;
line(xcen,0,xcen,getmaxy());
line(0,ycen,getmaxx(),ycen);
circle(xcen,ycen,200);
rectangle(xcen-200,ycen-200,xcen+200,ycen+200);
rectangle(xcen-120,ycen-180,xcen+120,ycen+180);
ellipse(xcen,ycen,0,360,50,100), 
getch();
closegraph(); 
}
```

## PRACTICAL  7
#### AIM: Draw the colour rainbow animation on the screen.
 ```
#include<graphics.h>
#include<conio.h>
void main()
{
int gd=DETECT,gm,x,y;
initgraph(&gd,&gm,"C:\\TURBOC3\\BGI");
x=getmaxx()/2;
y=getmaxy()/2;
for(i=30;i<200;i++)
delay(100);
setcolor(i/10);
arc (x,y,0,180,i-10); 
getch();
closegraph();
}
```
## PRACTICAL  8
#### AIM:To create and move the car
```
#include <graphics.h>
#include <conio.h>
#include <dos.h>

void drawCar(int x, int y) {
    // Body of the car
    rectangle(x, y, x + 100, y + 40);
    rectangle(x + 20, y - 20, x + 80, y);
    
    // Wheels of the car
    circle(x + 25, y + 40, 10);
    circle(x + 75, y + 40, 10);
    
    // Filling colors
    setfillstyle(SOLID_FILL, RED);
    floodfill(x + 1, y + 1, WHITE);
    
    setfillstyle(SOLID_FILL, BLUE);
    floodfill(x + 21, y - 1, WHITE);
    
    setfillstyle(SOLID_FILL, BLACK);
    floodfill(x + 25, y + 40, WHITE);
    floodfill(x + 75, y + 40, WHITE);
}

int main() {
    int gd = DETECT, gm;
    initgraph(&gd, &gm, "C:\\TURBOC3\\BGI");

    int x = 50, y = 300; // Starting position of car
    
    while (!kbhit()) {  // Loop until a key is pressed
        cleardevice();  // Clear screen
        
        drawCar(x, y);  // Draw car at position (x, y)
        
        delay(50);  // Small delay for smooth motion
        x += 5;     // Move car to the right
        
        if (x > getmaxx())  // Reset if car reaches end
            x = -100;
    }

    closegraph();
    return 0;
}
```