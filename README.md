# WebdriverIO
Based on WebdriverIO Tutorials by Raghav Pal 

https://www.youtube.com/playlist?list=PLhW3qG5bs-L9K2xtu-04jZFqykzXzqJW8

### To use this project

Step 1 - Download the folder or clone the repository

Step 2 - Check node.js is installed on your system  **`node -v`**

Step 3 - Open terminal/cmd > Goto project folder > Run command 

**`npm install`**	// this will download and install all required libraries mentioned in package.json file

**`npx wdio`**		// this will run the tests


### Project Setup & WebdriverIO Installation

Step 1 - Create a new folder and open in IDE (VS Code)

Step 2 - Open terminal in VS Code and run commands  	**`npm init -y`**  and  **`npm init wdio`**
                          
Step 3 - Select the options as required and install

Step 4 - Check WebdriverIO version 					**`npm ls webdriverio`**

Step 5 - Check wdio.conf.js file and project folders are created

Step 6 - To run existing tests

Run all tests in the folder configured in wdio.conf.js 	**`npx wdio run wdio.conf.js`**

or

**`npm run wdio`**

Run specific tests	 **`npx wdio run wdio.conf.js --spec test1.js`**



### How to create Tests

Step 1 - Create a new file under spec folder

Step 2 - Add the test script using it block (mocha)	

***
```
describe('Demo Tests', () => {
   it('My 1st Test', async () => {
       browser.url('https://google.com/')
       browser.pause(2000)
       await $('[name="q"]').setValue("WebdriverIO");
       await $('button[type="submit"]').click();
       browser.keys('Enter')
   })
})
```
***

$()   Single dollar sign to find a single web element

$$() Double dollar sign to find multiple web elements



### How to Generate and View Reports

Step 1 - Run - **`npm install @wdio/allure-reporter --save-dev`**

Step 2 - Add reporter config in wdio.conf.js

Step 3 - Run test and check Allure Results folder is generated

Step 4 - Install allure command line tool  npm install -g allure-commandline --save-dev

Step 5 - Run commands
		**`allure generate allure-results`**	// this will generate allure-report folder
		**`allure open`**			// will start server and open report

Refer - https://webdriver.io/docs/allure-reporter/



### How to RECORD WebdriverIO Test

Chrome DevTools Recorder - If you are using latest chrome  you will have the Recorder already installed and available   This feature is available only in Chrome, not Chromium


Step 1 - Open any website, do a Right-Click and select "Inspect"

Step 2 - To open Recorder panel - 

Click on More options       > More tools > Recorder

OR Click on More options      > Run Command > Show Recorder

Step 3 - Click on "Start new recording" > give your test a name and then use the browser to record test

Step 4 - Stop recording & click on "Replay" to check if the recording was successful 

Step 5 - Can Slowdown replay | Simulate network | Measure performance | Add Remove Edit steps | Edit locators

Step 6 - Can import | export steps

Step 7 - Can export for different tools using their chrome plugins - https://goo.gle/recorder-extension  e.g. 
Cypress Chrome Recorder  |  Nightwatch Chrome Recorder  |  Webdriver IO Chrome Recorder
__________________________

#### Never Stop Learning
***Raghav Pal***

***https://automationstepbystep.com/***

