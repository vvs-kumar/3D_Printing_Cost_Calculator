package cost_for_3dp;

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.io.File;

public class frame1 extends JFrame
{
   TextField  tf1;
   TextField  tf2;
   TextField  tf3;
   TextField  tf4;
   TextField  tf5;
   TextField  tf6;
   Button b;

                frame1()
                {


                    setLocation(600,200);
                    setTitle("Cost For 3D Printer.");

                    tf1= new TextField("Enter the Cost Of Material");
                    tf1.setBounds(50,50,200,20);
                    tf2= new TextField("Enter the Time of  printing of the material in Hours");
                    tf2.setBounds(50,100,200,20);
                    tf3= new TextField("Enter the finishing cost");
                    tf3.setBounds(50,150,200,20);
                    tf4= new TextField("Enter the other expences cost");
                    tf4.setBounds(50,200,200,20);
                    tf5= new TextField("Enter profit  percentage (Ex:0.25)");
                    tf5.setBounds(50,250,200,20);
                    tf6= new TextField("Enter the Human Cost(If no enter 0)");
                    tf6.setBounds(50,300,200,20);

                    b=new Button("Total Cost");
                    b.setBounds(50,350,85,20);

                    Label l1 = new Label("");


                    add(tf1);
                    add(tf2);
                    add(tf3);
                    add(tf4);
                    add(tf5);
                    add(tf6);
                    add(b);
                    add(l1);


                    setSize(300,470);
                    setVisible(true);

                    b.addActionListener(new ActionListener()
                    {
                        public void actionPerformed(ActionEvent e)
                        {
                            int a=Integer.parseInt(tf1.getText());
                            double b=Double.parseDouble(tf2.getText());
                            int c=Integer.parseInt(tf3.getText());
                            int d=Integer.parseInt(tf4.getText());
                            double g=Double.parseDouble(tf5.getText());

                            int f=Integer.parseInt(tf6.getText());
                            double j=(2.3334*b);
                            double h=a+j+c+d+f;


                            double t=g*h;

                            double out1=h+t;
                            l1.setBounds(50,400,85,20);
                            l1.setText("Cost "+ String.valueOf(out1));


                            setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
                            setLocation(229,300);
                            ImageIcon img =new ImageIcon("‪C:/Users/VVS/Pictures/vvs.png");
                            setIconImage(img.getImage());

                        }
                    });
                }

                public static void main(String arg[])
                {

                    new frame1();



                }
}
