# Introduction to JavaScript:

JavaScript is a versatile programming language commonly used for web 
development. It allows you to add interactivity, animations, and dynamic 
behavior to websites. It can also be used on the server-side using a 
runtime environment called Node.js.

# Setting Up Node.js Environment on Windows 10:

-- Step 1: Install Node.js:

   1. Open web browser and go to the official Node.js website: https://nodejs.org/

   2. On the homepage, you'll see two versions available: 
      LTS (Long Term Support) and Current. For beginners, 
      it's recommended to go with the LTS version, as it's 
      more stable. Click on the "LTS" button to download it.

   3. Once the installer is downloaded, double-click on it to run it.

   4. Follow the installation wizard's instructions. You can usually 
      leave the default settings as they are.

   5. After installation, you can verify if Node.js was installed 
      successfully by opening the Command Prompt (search for "cmd" 
      in the Start menu), and typing:

      ```node -v```

      This should display the version number of Node.js that you installed.

-- Step 2: Verify npm (Node Package Manager):

   npm comes bundled with Node.js and is used to install libraries 
   (packages) that extend the functionality of Node.js and JavaScript.

   1. In the same Command Prompt, type:

      npm -v

      This should display the version of npm that was installed.

-- Step 3: Set Up a Test JavaScript File:

   1. Create a new folder on your computer where you'll practice your 
      JavaScript code. For example, you can create a folder named 
      "js-practice" on your desktop.

   2. Inside that folder, create a new file named "app.js". This is where 
      you'll write your JavaScript code.

-- Step 4: Write and Run Your First JavaScript Code:

   1. Open "app.js" using a text editor. You can use Notepad or even better,
      a code editor like Visual Studio Code (https://code.visualstudio.com/).

   2. Type the following code to print a simple message to the console:
      
      console.log("Hello, world!");

   3. Save the file.

-- Step 5: Run the JavaScript Code:

   1. Open Command Prompt and navigate to the folder where you saved "appjs". 
      You can use the cd command to change directories. For example:

      cd path/to/js-practice

   2. Once you're in the correct directory, type the following command to run your JavaScript file:

      node app.js

      You should see the output "Hello, world!" displayed in the console.

   Congratulations! You've successfully set up a Node.js environment 
   on Windows 10 and written and run your first JavaScript code.