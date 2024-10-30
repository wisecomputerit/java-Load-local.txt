Contribute code
<p>import java.io.BufferedWriter;</p>
<p>import java.io.FileWriter;</p>
<p>import java.io.IOException;</p>

public class WriteToFile {
    public static void main(String[] args) {
    
        String filePath = "output.txt"; // 你要寫入的文件路徑
        String content = "Hello, World!"; // 要寫入的內容

        try (BufferedWriter writer = new BufferedWriter(new FileWriter(filePath))) {
            writer.write(content); // 寫入內容
            writer.newLine(); // 換行
            writer.write("這是第二行。");
        } catch (IOException e) {
            e.printStackTrace(); // 處理異常
        }
    }
}
