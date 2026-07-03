import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class RadioButtonDemo extends JFrame {
    private final String[] petNames = {"Bird", "Cat", "Dog", "Rabbit", "Pig"};
    private JRadioButton[] radioButtons;
    private ButtonGroup group;

    public RadioButtonDemo() {
        setTitle("RadioButtonDemo");
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new FlowLayout(FlowLayout.LEFT, 20, 20));

        JPanel buttonPanel = new JPanel();
        buttonPanel.setLayout(new BoxLayout(buttonPanel, BoxLayout.Y_AXIS));

        group = new ButtonGroup();
        radioButtons = new JRadioButton[petNames.length];

        for (int i = 0; i < petNames.length; i++) {
            radioButtons[i] = new JRadioButton(petNames[i]);
            group.add(radioButtons[i]);
            buttonPanel.add(radioButtons[i]);

            radioButtons[i].addActionListener(new ActionListener() {
                @Override
                public void actionPerformed(ActionEvent e) {
                    JRadioButton source = (JRadioButton) e.getSource();
                    if (source.isSelected()) {
                        JOptionPane.showMessageDialog(
                                RadioButtonDemo.this,
                                "You selected: " + source.getText(),
                                "Pet Selection",
                                JOptionPane.INFORMATION_MESSAGE
                        );
                    }
                }
            });
        }

        add(buttonPanel);

        setSize(350, 200);
        setLocationRelativeTo(null); 
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(new Runnable() {
            @Override
            public void run() {
                new RadioButtonDemo().setVisible(true);
            }
        });
    }
}