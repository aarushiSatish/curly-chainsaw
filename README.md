# curly-chainsaw
import java.util.Random;
//Begin the class Pipes with the following code


import java.awt.*;

import java.awt.geom.Point2D;

import java.awt.geom.Line2D;
import javax.swing.*;

public class Pipes extends JFrame { 

public Pipes() { 

super("Pipes"); 

setSize(600, 600); 

setLocationRelativeTo(null);

setVisible(true); 

} 

public void paint(Graphics g) { 

super.paint(g); 


Random random = new Random(111);
Graphics2D g2d = (Graphics2D) g;
g2d.fillRect(0, 0,600,600);
g2d.setColor(Color.BLACK);
g2d.setStroke(new BasicStroke(5));  //thicker line
Point2D.Double point = new Point2D.Double(0,0);
Point2D.Double point1 = new Point2D.Double();
g2d.setColor(Color.white);

for (int i = 1;i<=10; i++)
{
    point1.setLocation(random.nextInt(600), random.nextInt(600));
    //int x1_loc = random.nextInt(i *100);
    //int x2_loc = random.nextInt(i*100);
    
    //int y1_loc = random.nextInt(i*100);
    //int y2_loc = random.nextInt(i*100);
    //point1.x = x1_loc;    
    //point1.y=y1_loc;
    try {

         Thread.currentThread().sleep(100);

    } catch (InterruptedException e){ 

        e.printStackTrace();

    }
    
    g2d.drawLine((int)point.getX(),(int)point.getY(),(int) point1.getX(), (int)point1.getY() );    
    point.setLocation(point1.getX(),point1.getY());
    //point1.x = point.getX();    
    //point1.y=point.getY();
    
}

//g2d.drawLine(10, 10, 10, 10);
  
Random random1 = new Random(111);
 //thicker line
Point2D.Double point2 = new Point2D.Double(0,0);
Point2D.Double point3 = new Point2D.Double();
g2d.setColor(Color.BLACK);

  for (int j= 1;j<=10; j++)
{
    point3.setLocation(random1.nextInt(600), random1.nextInt(600));
    //int x1_loc = random.nextInt(i *100);
    //int x2_loc = random.nextInt(i*100);
    
    //int y1_loc = random.nextInt(i*100);
    //int y2_loc = random.nextInt(i*100);
    
    //point1.x = x1_loc;    
    //point1.y=y1_loc;
    try {

         Thread.currentThread().sleep(100);

    } catch (InterruptedException e){ 

        e.printStackTrace();

    }
    
    g2d.drawLine((int)point2.getX(),(int)point2.getY(),(int) point3.getX(), (int)point3.getY() );    
    point2.setLocation(point3.getX(),point3.getY());
    //point1.x = point.getX();    
    //point1.y=point.getY();
    
}
}

//g2d.drawLine(10, 10, 10, 10);

   public static void main(String[] args)
   {
       Pipes pi = new Pipes();
       
   }
}
