# Replicating Develope Environment
## Getting access to the WordPress
- After obtaining administrator privilege, Log into the [WordPress editor](https://livetorock.org/wp-login.php?redirect_to=https%3A%2F%2Flivetorock.org%2Fwp-admin%2Fadmin.php%3Fpage%3Dbluehost&reauth=1).
    - This should be able to be accessed through any browser.

- Within the editor, the main area we're focusing on is in the plugins.
    - Time.ly handles the calendar widget on the website.
    - User Registration handles the user's ability to create an account on the server.
    - Akismet handles the anti-spam protection for the website.
    - Forums handles the forums and posts

- There is also the User section, this will allow us to edit the user's roles and access to different parts of the site.

- On the areas of the editor, the "Pages" section will let us see all the pages of the website and allow us to edit them.

- There is an area on the main page of the editor called "Staging" which allows us to make a feature branch for the website to build on.

## Installing WP, PHP, and MySQL
- First step that covers most of the process, install [Apache](https://www.apachefriends.org/) with the default settings.

- After it installs, open the control panel and start Apache and MySQL. (If you have a past version of MySQL, you may have to change the ports to access 3307 or uninstall the old version)

- Now that those are started, click Admin next to MySQL and it will load the database on your local host.

- In here, you're going to create a new database and can be named anything for example "mywordpress."

- Then, you will have to download [WordPress](https://wordpress.org/download/) and extract the files, remove one of the compounded folders (there should be 1 file with everything directly inside it), and rename the file "mywordpress."

- You will want to move the "mywordpress" file into your C drive > xampp > htdocs.

- Then open a new tab in your browser and go to "localhost/mywordpress" then go through the steps of installing WordPress.
    - Select language
    - Click "Let's go"
    - Fill database name "mywordpress", username, and password
    - Run installation

- Then make a site title, input another username (can be same or different), same with password, your email, and install.
