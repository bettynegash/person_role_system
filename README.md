import javax.swing.*;
import java.io.*;

public class NotepadApp {

    public static void main(String[] args) {

        JFrame frame = new JFrame("Simple Notepad");

        JTextArea textArea = new JTextArea();
        JScrollPane scrollPane = new JScrollPane(textArea);

        JMenuBar menuBar = new JMenuBar();

        JMenu fileMenu = new JMenu("File");

        JMenuItem newItem = new JMenuItem("New");
        JMenuItem openItem = new JMenuItem("Open");
        JMenuItem saveItem = new JMenuItem("Save");
        JMenuItem exitItem = new JMenuItem("Exit");

        fileMenu.add(newItem);
        fileMenu.add(openItem);
        fileMenu.add(saveItem);
        fileMenu.addSeparator();
        fileMenu.add(exitItem);

        menuBar.add(fileMenu);

        frame.setJMenuBar(menuBar);

        frame.add(scrollPane);

        // New
        newItem.addActionListener(e -> textArea.setText(""));

        // Open
        openItem.addActionListener(e -> {
            JFileChooser chooser = new JFileChooser();

            if (chooser.showOpenDialog(frame) == JFileChooser.APPROVE_OPTION) {

                File file = chooser.getSelectedFile();

                try (BufferedReader reader =
                             new BufferedReader(new FileReader(file))) {

                    textArea.setText("");

                    String line;

                    while ((line = reader.readLine()) != null) {
                        textArea.append(line + "\n");
                    }

                } catch (IOException ex) {
                    ex.printStackTrace();
                }
            }
        });

        // Save
        saveItem.addActionListener(e -> {
            JFileChooser chooser = new JFileChooser();

            if (chooser.showSaveDialog(frame) == JFileChooser.APPROVE_OPTION) {

                File file = chooser.getSelectedFile();

                try (BufferedWriter writer =
                             new BufferedWriter(new FileWriter(file))) {

                    writer.write(textArea.getText());

                } catch (IOException ex) {
                    ex.printStackTrace();
                }
            }
        });

        // Exit
        exitItem.addActionListener(e -> System.exit(0));

        frame.setSize(600, 400);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
