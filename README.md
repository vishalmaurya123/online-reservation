
import java.awt.event.*; 
import java.awt.*; 
 
import javax.swing.*; 
public class project extends JFrame  implements ActionListener 
{ 
JButton employee; 
JButton reserve,train_info; 
JButton reserved_status; 
JPanel main; 
ImageIcon img; 
 
public project() 
{ 
 this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); 
img=new ImageIcon("/home/nitesh/Programming/Java Rdmbs project/logo.jpg"); 
main=new JPanel(); 
employee=new JButton("Enter As Employee"); 
train_info=new JButton("Train Enquiry"); 
reserve=new JButton("Reserve Seats"); 
reserved_status=new JButton("Reservation Status"); 
 
main.add(employee); 
main.add(train_info); 
main.add(reserve); 
main.add(reserved_status); 
 
this.add(img); 
this.add(main); 
this.setSize(1000,1000); 
 
 
employee.addActionListener(this); 
train_info.addActionListener(this); 
reserve.addActionListener(this); 
reserved_status.addActionListener(this); 
 
 
 
pack(); 
this.setVisible(true); 
this.setTitle("Railway Reservation"); 
 
 
} 
 
 
 
private void add(ImageIcon img2) { 
  
 
 
} 
 
 
 
 
public void actionPerformed(ActionEvent ex) 
{ 
String s=ex.getActionCommand(); 
if(s.equals("Enter As Employee")) 
{ 
 
 employee e=new employee(); 
 e.setVisible(true); 
 this.setVisible(false);  
} 
else if(s.equals("Train Enquiry")) 
{ 
 
 traininfo t=new traininfo(); 
 this.setVisible(false); 
 t.setVisible(true); 
  
} 
else if(s.equals("Reserve Seats")) 
{ 
   
reserve r =new reserve(); 
r.setVisible(true); 
this.setVisible(false); 
 
} 
else if(s.equals("Reservation Status")) 
{ 
  
status st=new status(); 
st.setVisible(true); 
this.setVisible(false); 
} 
 
} 
 
 
public static void main (String args[]) 
{ 
  SwingUtilities.invokeLater(new Runnable() 
  { 
   public void run() 
   { 
    new project(); 
   } 
  }); 
  
  
  
  
} 
 
}
