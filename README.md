# biztream

package org.openqa.selenium;



    
    import org.openqa.selenium.WebDriver;
    import org.openqa.selenium.WebElement;

import java.util.concurrent.TimeUnit;

import org.apache.xerces.impl.xpath.XPath;
import org.openqa.selenium.By;
    import org.openqa.selenium.chrome.ChromeDriver;




        public class Facebook
       {

        public static void main(String[] args) throws InterruptedException {
       

        	System.setProperty("webdriver.chrome.driver", "C:\\chromedriver_win32\\chromedriver.exe");

        WebDriver driver = new ChromeDriver();
        String baseWindowHdl = driver.getWindowHandle();



        driver.get("http://my.biztream.com");


        WebElement element1 = driver.findElement(By.id("username_id"));
        element1.sendKeys("p1k@gmail.com");

        WebElement element2 = driver.findElement(By.id("password_id"));
        element2.sendKeys("123");

        WebElement element3 = driver.findElement(By.name("Login"));
        element3.click();
        
              
        driver.findElement(By.id("loginSelectDiv1")).click();
        
       driver.manage().window().maximize();
        Alert alert=driver.switchTo().alert();
        alert.dismiss();

