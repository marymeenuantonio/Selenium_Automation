# Selenium_Automation
A basic Selenium test using Java

This repository contains a basic automated test using **Selenium with Java**.  
It’s a simple demonstration to show how a web page can be tested using automation tools.

---

## 💻 Test Code (Java + Selenium)

```java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class SimpleTest {
    public static void main(String[] args) {
        System.setProperty("webdriver.chrome.driver", "path/to/chromedriver");
        WebDriver driver = new ChromeDriver();

        driver.get("https://example.com");

        WebElement heading = driver.findElement(By.tagName("h1"));
        if (heading.getText().equals("Example Domain")) {
            System.out.println("✅ Test Passed!");
        } else {
            System.out.println("❌ Test Failed!");
        }

        driver.quit();
    }
}
