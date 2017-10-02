import java.awt.*;
 
 public class FallingCube
 {
 	private final int xLeft; 
 	private final int cubeSize;
 	private int cubeX, cubeY;
 	private int yStep; 
 	private static final String letters="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
 	private char randomLetter; //Cube letter
 	
 public FallingCube(int size,int x)
 	{
 	cubeSize=size;
 	xLeft=x;
 	yStep=cubeSize/8;
 	cubeX=-cubeSize;
 	cubeY=-cubeSize;
 	}
 public void start()
 	{
 	int i=(int)(Math.random()*letters.length());
 	randomLetter=letters.charAt(i);
 	cubeX=0;
 	cubeY=-cubeSize;
 	}
 public boolean moveDown()
 	{
 	if (cubeY<6*cubeSize)
 	{
 		cubeY+=yStep;
 		return true;
 	}
 	else //land this cube;	
 	{
 		return false;
 	}
 }
  	
 public void draw(Graphics g)
{
 	int x=xLeft+cubeX;
 	int y=cubeY;
 	int c=(int)(Math.random()*5+1);
 	Color b=Color.white;
 	if (c==1){
 		b=Color.blue;
 	}
 	if (c==2){
 		b=Color.cyan;
 	}
 	if (c==3){
 		b=Color.yellow;
 	}
 	if (c==4){
 		b=Color.pink;
 	}
 	if (c==5){
 		b=Color.orange;
 	}
 	g.setColor(Color.red);
 	g.fill3DRect(x,y,cubeSize-1,cubeSize-1,true);
 	g.setColor(b);
 	g.fillRoundRect(x+5,y+5,cubeSize-10,cubeSize-10, cubeSize/2-5,cubeSize/2-5);
 	g.setColor(Color.darkGray);
 	String s=String.valueOf(randomLetter);
 	g.drawString(s,x+cubeSize/2-6,y+cubeSize/2+5);
}	
 }
  	
