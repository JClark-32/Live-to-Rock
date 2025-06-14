# Manual Install
## Installing WP, PHP, and MySQL
- First step that covers most of the process, install [Apache](https://www.apachefriends.org/) with the default settings.

- After it installs, open the control panel and start Apache and MySQL. (If you have a past version of MySQL, you may have to change the ports to access 3307 or uninstall the old version)

- Now that those are started, click Admin next to MySQL and it will load the database on your local host.

- In here, you're going to create a new database and can be named anything for example `mywordpress.`

- Then, you will have to download [WordPress](https://wordpress.org/download/) and extract the files, remove one of the compounded folders (there should be 1 file with everything directly inside it), and rename the file `mywordpress.`

- You will want to move the `mywordpress` file into your C drive > xampp > htdocs.

- Then open a new tab in your browser and go to "localhost/mywordpress" then go through the steps of installing WordPress.
    - Select language
    - Click "Let's go"
    - Fill database name `mywordpress`, username, and password
    - Run installation

- Then make a site title, input another username (can be same or different), same with password, your email, and install.

## Adding the plugin to your website
- Clone the github using `git clone https://github.com/JClark-32/Live-to-Rock-Source-Code.git` in Git Bash.

- Then locate the LifePerformancesPlugin folder.

- Take the plugin file and copy it onto your clipboard.

- Open your website folder: C drive > xampp > htdocs > `mywordpress` > wp-content > plugins > paste plugin file here.

- Now go to your local website and go to the plugin tab.

- Activate the plugin that you just added.

- Implement plugin features as needed, for example: in Life Performance, you need to add a "shortcode" to the page.

## Getting access to the WordPress
- After obtaining administrator privilege, Log into the [WordPress editor](https://livetorock.org/wp-login.php?redirect_to=https%3A%2F%2Flivetorock.org%2Fwp-admin%2Fadmin.php%3Fpage%3Dbluehost&reauth=1).
    - This should be able to be accessed through any browser.

- Within the editor, the main area we're focusing on is in the plugins.
    - Time.ly handles the calendar widget on the website.
    - User Registration handles the user's ability to create an account on the server.
    - Akismet handles the anti-spam protection for the website.
    - Forums handles the forums and posts.

- There is also the "User" section, this will allow us to edit the user's roles and access to different parts of the site.

- On the areas of the editor, the "Pages" section will let us see all the pages of the website and allow us to edit them.

- There is an area on the main page of the editor called "Staging" which allows us to make a feature branch for the website to build on.

# Docker install
## Download
- For simplicity, we're gonna be using [Docker Desktop](https://www.docker.com/products/docker-desktop/).
    - We are currently using, Docker version 27.3.1.

- After installing, you'll want to clone the repository using `git clone https://github.com/JClark-32/Live-to-Rock-Source-Code.git` in Git Bash.

- Now that it's cloned, locate the `docker-compose.yml` (this might say .yaml, there is no notable difference). 
    - Make a new folder where you want to store the project and open the folder in VSCode.
    - Run this file in VSCode using the terminal and calling, `docker-compose.yml up -d`.
    - As this loads, you'll begin to see files populate on the side of the screen.

## Docker Image
- After running the .yml file, inside your docker desktop app, you should have an image already running.
    - This image will be running and will allow you to access the wordpress website on your local host.
    - You should be able to access this at `localhost:8080` in your browser.

## Adding the Plugin
- You'll want to clone the github using `git clone https://github.com/JClark-32/Live-to-Rock-Source-Code.git` in Git Bash.
    - Then locate the folder for the plugin you're adding for example `LifePerformancesPlugin`.
    - Take the plugin file and copy it onto your clipboard.

- There are 2 ways to add the plugin.
    - First, inside VSCode there is a folder that was created called `wp-content` and inside that is another folder called `plugins`.
        - Inside here, you'll want to paste the `LifePerformancesPlugin` folder so it gets added to the website.

    - Second, on the website itself, you'll go to the plugin section and press the "Add New Plugin" then upload the `LifePerformancesPlugin` folder in a zip file.
 
# Composer Install

## Setting Up Testing 

- Create a workspace.

- Start by cloning the repository using `git clone https://github.com/JClark-32/Live-to-Rock-Source-Code.git` in Git Bash.

## Install Composer and Set Up PHPUnit

- Install [Composer 2.8.6](https://getcomposer.org/download/) here.

- Install PHPUnit 11.4 using Composer in the command line via `composer require --dev phpunit/phpunit`
    - If any errors occur, try `composer dump-autoload`

- Then to run the tests, use the command `vendor/bin/phpunit.\tests\Unit\` to run all tests.

- `vendor/bin/phpunit.\tests\Unit\LifePerformancesTests\` to run the LifePerformance plugin tests.

- `vendor/bin/phpunit.\tests\Unit\JamSessionTests\` to run the JamSession plugin tests.

- If you want to run specific tests, example: `vendor/bin/phpunit .\tests\Unit\LifePerformancesTests\SendEmailToAdminTest.php`.

## Setting up Code Coverage

- Open command prompt

- Enter `php -i`

- Copy all of that (it's A LOT, sorry)

- Go to [xdebug](https://xdebug.org/wizard)

- Paste that into the box and click the analyze button

- Download the `php_xdebug-3.4.2-8.3-ts-vs16-x86_64.dll` provided to you on the next page

- Move the downloaded file to ext, and rename it to `php_xdebug.dll`

- Cut that file and go to wherever your PHP install is (mine is right under C: as php.(whatever version, mine's 8. something))

- Go to the ext subfolder

- Paste that renamed file in there

- Open `C:\php-8.3.13[or whatever ur version is]\php.ini`  in something like Notepad++

- `Ctrl+f then zend_ext` until you find `;zend_extension = something`

- Replace that with the following:
- [Xdebug]
- `zend_extension="C:\path\to\php\ext\xdebug.dll"`
- `xdebug.mode=coverage,debug`
- `xdebug.start_with_request=yes`

- Save!

- Restart Docker

- Run `php -v` in the cmd and make sure it pops up with an xdebug version

- Make sure you have the latest version from development

- Run `vendor/bin/phpunit .\tests\Unit\ --coverage-text` in the project

- Yay! You (should have) done it

# Getting and Setting New Youtube API Key
## Log Into the Google API Developer Console

- Go to [The Google API Devloper Console](https://console.cloud.google.com/apis/dashboard)
- Sign into the account you want the API key on
- Select the Back Stage Pass Plugin Project, If it doesn't exist press create project and create one with that name

## Enable the YouTube Data API V3

- On the left hand side navigation bar select APIs & Services
- On the left hand side of that page select the Enabled APIs & Services tab
- On the top bar there is a button labeled +Enable APIs and services, click that
- Search for YouTube Data API v3, select the result, and then press enable

## Create the API Key and Restrict it

- Go back to the APIs & Services page
- Select the credentials tab
- On the top bar, select create credentials
- Select API key
- You will now see an API key 1 under the API Keys section
- Press the 3 buttons under actions and select Edit API key
- Under API restrictions select restrict key
- In the drop down box select YouTube Data API v3 and press ok
- Save the settings

## Utilize the new API Key

- Press the Show Key button and copy the API Key
- Insert this into line 63 of BackStagePassPlugin.php making sure to replace the old API key

