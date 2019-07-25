# [DEPRICATED]
## Please follow https://github.com/allure-framework/allure-java
Allure Cucumber-JVM Plugin
=====================

This plugin allows to generate allure xml reports after cucumber-jvm tests execution.

## Example project
Example projects is located at: https://github.com/spt110/allure-cucumber3-plugin

## Usage
Simply add **allure-cucumber3-plugin** as dependency to your project and add **build** section with adaptor plugin: 
```
package myCucumber

import org.junit.runner.RunWith;
import cucumber.api.CucumberOptions;
import cucumber.api.junit.Cucumber;
import cucumber.api.java.After;
import cucumber.api.java.Before;
import AllureCucumber3Jvm
@RunWith(Cucumber.class)
@CucumberOptions(features="Include/features", glue="", plugin = ["pretty",
	"junit:report-cucumber/cucumber.xml",
	"html:report-cucumber/cucumber-html-report",
	"json:report-cucumber/cucumber.json",
	"AllureCucumber3Jvm"
])
public class BillInvoiceCucumberRunner {

	//		@Before
	//		public void before() {
	////			AllureReporter.applyFailureCallback(FailureCallback.class);
	//		}
	//
	//
	//
	//	@After
	//	public void after() {
	//		int result = AllureReporter.getFailureCallbackResult();
	//		Assert.assertEquals(10, result);
	//	}
}
```