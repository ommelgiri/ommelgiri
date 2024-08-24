- 👋 Hi, I’m @ommelgiri
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
ommelgiri/ommelgiri is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class SimpleForm {

    public static void main(String[] args) {
        // Create a frame
        JFrame frame = new JFrame("Simple Form");
        frame.setSize(300, 200);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setLayout(null);

        // Create and set up components
        JLabel nameLabel = new JLabel("Name:");
        nameLabel.setBounds(10, 20, 80, 25);
        frame.add(nameLabel);

        JTextField nameTextField = new JTextField();
        nameTextField.setBounds(100, 20, 165, 25);
        frame.add(nameTextField);

        JButton submitButton = new JButton("Submit");
        submitButton.setBounds(10, 80, 80, 25);
        frame.add(submitButton);

        // Add action listener to the button
        submitButton.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                String name = nameTextField.getText();
                JOptionPane.showMessageDialog(frame, "Hello, " + name + "!");
            }
        });

        // Make the frame visible
        frame.setVisible(true);
    }
}
