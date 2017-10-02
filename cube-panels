import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class LetterPanel extends JPanel
		implements ActionListener
		{
		private FallingCube cube,cube2;
		private final int CUBESIZE=40;
		private final int delay=30;
		private Timer t;
	public LetterPanel()
	{
		cube=new FallingCube(CUBESIZE,100);
		t=new Timer(delay,this);
	}
	public void dropCube()
	{
		cube.start();
		t.start();
	}
	
public void actionPerformed(ActionEvent e)
	{
		boolean moved=cube.moveDown();
		if (!moved) {	
			t.stop();
		}

		repaint();
	}
	public void paintComponent (Graphics g)
	{
		super.paintComponent(g);
		cube.draw(g);	
	}
}
  
