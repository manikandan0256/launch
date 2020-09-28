# launch
package com.etsy.resources;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class FunctionalLibrary {
	public static void main(String[] args) {

		System.setProperty("webdriver.chrome.driver", "E:\\Mani\\Assign\\resources\\lib\\chromedriver.exe");

		WebDriver driver = new ChromeDriver();
		driver.get("http://stage-newstuck.onemindindia.com/#/login");
		driver.manage().window().maximize();
		driver.navigate().refresh();
		WebElement usname = driver.findElement(By.className("//input[@formcontrolname='username']"));
		usname.sendKeys("StageCurator");
		WebElement Pwd = driver.findElement(By.xpath("//input[@placeholder='Password']"));
		Pwd.sendKeys("$tageN3w5tuckCu6ato6");
		WebElement submit = driver.findElement(By.xpath("//input[@type='submit']"));
		submit.click();

	}
}
