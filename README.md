# TwitteTestCase
module not found



package basicTest;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver; // import web driver
import org.openqa.selenium.chrome.ChromeDriver; //import chrome driver

public class LoginTest {

	public static void main(String[] args) {
		
		// setup the path for chrome driver
		System.setProperty("webdriver.chrome.driver","C://chromedriver_win32/chromedriver.exe"); 
		
		//initialzing the chrome driver
		WebDriver driver=new ChromeDriver();
		
       // providing the url 
		driver.get("https://twitter.com/LOGIN");
		
		// find web element by username and input username
		driver.driver.findElement(By.name("session[username_or_email]")).sendKeys("user");
		
		//  find web element by username and input password
		driver.driver.findElement(By.name("session[password]")).sendKeys("pass");
		
		//  find web element by linktext and click login button
		driver.findElement(By.linkText("Log in")).click();
		String exp_title = "Twitter";
		String act_title = driver.getTitle();
		
		// comparing actual title and expected tile of web page
		if(act_title.equals( exp_title)==true)
		{
			System.out.println("pass");
		}
		else
		{
			System.out.println("fail");
		}
		driver.close();
	}

}
