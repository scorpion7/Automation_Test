Automation_Test
===============
//Sample Web driver Scripts for Automating Login and Logout from Gmail
//@author  Mahendra

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class Web_Driver {

	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub

		WebDriver driver = new FirefoxDriver();
		driver.get("http://www.gmail.com");
		WebElement element = driver.findElement(By.id("Email"));
		Thread.sleep(3000);
		element.sendKeys("TEST_EMAIL_ID_HERE@gmail.com");
		driver.switchTo();

		WebElement element1= driver.findElement(By.id("Passwd"));
		Thread.sleep(3000);
		element1.sendKeys("TEST_EMAIL_PASSWORD_HERE");
		driver.switchTo(); 

		Thread.sleep(3000);
		driver.findElement(By.id("signIn")).click(); //click to sign in

		Thread.sleep(3000);
		driver.findElement(By.id("gbgs4")).click();

		Thread.sleep(3000);
		driver.findElement(By.id("gb_71")).click();

		Thread.sleep(3000);
		driver.close();

	}

}
