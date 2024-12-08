Attendence Management System 
Using JAVA - GUI - CSV and TXT
This project is for Educational Purposes only.

> Program:

        package pkg;
        import javax.swing.*;
        import java.awt.*;
        class Excel_handling extends ClassNotFoundException {
	static class RoundedButton extends JButton {                                                
        public RoundedButton(String text) {
            super(text);
            setContentAreaFilled(false);
        }        
	
        protected void paintComponent(Graphics g) {
            Graphics2D g2 = (Graphics2D) g.create();
            g2.setRenderingHint(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON);

            // Draw button background
            g2.setColor(new Color(0, 123, 255));
            g2.fillRoundRect(0, 0, getWidth(), getHeight(), 40, 40);

            // Draw button text
            g2.setColor(Color.WHITE);
            FontMetrics fm = g2.getFontMetrics();
            int textWidth = fm.stringWidth(getText());
            int textHeight = fm.getAscent();
            g2.drawString(getText(), (getWidth() - textWidth) / 2, (getHeight() + textHeight) / 2 - 3);

            g2.dispose();
        }

        @Override
        public void setContentAreaFilled(boolean b) {
        }
    }

	public static void main(String[] args) {
        JFrame frame = new JFrame("Attendance Management System");
        frame.setExtendedState(JFrame.MAXIMIZED_BOTH);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JPanel backgroundPanel = new JPanel() {
            @Override
            protected void paintComponent(Graphics g) {
                super.paintComponent(g);
                Graphics2D g2 = (Graphics2D) g;
                g2.setRenderingHint(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON);

                GradientPaint gradient = new GradientPaint(0, 0, new Color(135, 206, 235),
                        getWidth(), getHeight(), new Color(25, 25, 112));
                g2.setPaint(gradient);
                g2.fillRect(0, 0, getWidth(), getHeight());
            }
        };
        backgroundPanel.setLayout(new GridBagLayout());
        frame.add(backgroundPanel);

        JPanel centralPanel = new JPanel(new GridBagLayout()) {
            @Override
            protected void paintComponent(Graphics g) {
                super.paintComponent(g);
                Graphics2D g2 = (Graphics2D) g;
                g2.setRenderingHint(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON);

                g2.setColor(new Color(255, 255, 255, 200));
                g2.fillRoundRect(0, 0, getWidth(), getHeight(), 50, 50);
            }
        };
        centralPanel.setOpaque(false); 
        GridBagConstraints gbc = new GridBagConstraints();
        gbc.insets = new Insets(20, 20, 20, 20);

        JLabel label = new JLabel("Choose Access: ");
        label.setFont(new Font("Arial", Font.BOLD, 30));
        label.setForeground(new Color(25, 25, 112));

        String[] options = {"Admin", "Student"};
        JComboBox<String> accessChoice = new JComboBox<>(options);
        accessChoice.setFont(new Font("Arial", Font.PLAIN, 25));
        accessChoice.setPreferredSize(new Dimension(220, 50));

        RoundedButton accessButton = new RoundedButton("Submit");
        accessButton.setFont(new Font("Arial", Font.BOLD, 25));
        accessButton.setPreferredSize(new Dimension(220, 50));

        gbc.gridx = 0;
        gbc.gridy = 0;
        centralPanel.add(label, gbc);

        gbc.gridx = 1;
        gbc.gridy = 0;
        centralPanel.add(accessChoice, gbc);

        gbc.gridx = 1;
        gbc.gridy = 1;
        centralPanel.add(accessButton, gbc);

        backgroundPanel.add(centralPanel);

        accessButton.addActionListener(e -> {
            String choice = (String) accessChoice.getSelectedItem();
            if ("Admin".equals(choice)) {
                new Adminss().access();
            } else if ("Student".equals(choice)) {
                new Studentss().access();
            }
        });

        frame.setVisible(true);
    }}
