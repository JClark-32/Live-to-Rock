# Replicating Develope Environment
## Getting access to the WordPress
- After obtaining administrator privilege, Log into the [WordPress editor](https://livetorock.org/wp-login.php?redirect_to=https%3A%2F%2Flivetorock.org%2Fwp-admin%2Fadmin.php%3Fpage%3Dbluehost&reauth=1).
    - This should be able to be accessed through any browser.

- Within the editor, the main area we're focusing on is in the plugins.
    - Time.ly handles the calendar widget on the website.
    - User Registration handles the user's ability to create an account on the server.
    - Akismet handles the anti-spam protection for the website.

- There is also the User section, this will allow us to edit the user's roles and access to different parts of the site.

- On the areas of the editor, the "Pages" section will let us see all the pages of the website and allow us to edit them.

- There is an area on the main page of the editor called "Staging" which allows us to make a feature branch for the website to build on.

## Installing PHP
- To get started you want to head to [PHP](https://windows.php.net/download#php-8.3) and download PHP 8.3.13 Thread Safe.

- After that downloads, you will extract it and move it into your C drive. Then you'll rename the file so it only has "php-8.3.13" and copy its path.

- Then you'll open up your environment variables and find your "path" and click edit.

- On the edit screen, you'll select a blank spot and paste the php path, then you can test in your command line that it installed using php --version.

- Once that has been complete, you will need to install [Visual Studio Code](https://code.visualstudio.com).

- Inside VSCode, you will need to open File > Preferences > Settings > Extensions > PHP and open the JSON settings document and paste your php path in the executable string.

- Once you run a php program, it will have you install a debugger and then you will need to repeat the previous step but for the debugger string.