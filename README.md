# dd_tests
This file contains the code for the test cases
package dd_tests;

import org.openqa.selenium.By;
import org.openqa.selenium.support.ui.Select;
import org.testng.annotations.Test;

import dd_core.TestCore;

public class LoginTest extends TestCore
{
    @Test
	public void doLogin() throws InterruptedException
	{
		
		driver.findElement(By.xpath(object.getProperty("username"))).sendKeys("superadmin");
		driver.findElement(By.xpath(object.getProperty("password"))).sendKeys("U Shall n0t PASS!");
		Select options =  new Select(driver.findElement(By.xpath(object.getProperty("domain"))));
        options.selectByIndex(1);
        driver.findElement(By.xpath(object.getProperty("login"))).click();
        Thread.sleep(3000);
		
		
	}
	
	
	
	
	
}
