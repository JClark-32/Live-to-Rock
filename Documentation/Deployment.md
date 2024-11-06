## Deploying a Plug In

#### Prerequisites 
What needs to be installed before starting: Apache Web Server, MySQL, VSCODE

##### Your local machine. 
1.  Install [Apache](https://www.apachefriends.org/) with the default settings.
    
2. Open the control panel and start Apache and MySQL. (If you have a past version of MySQL, you may have to change the ports to access 3307 or uninstall the old version)

3. Now that those are started, click Admin next to MySQL and it will load the database on your local host.

4. In here, you're going to create a new database and can be named anything for example "mywordpress."

5. Then, you will have to download [WordPress](https://wordpress.org/download/) and extract the files, remove one of the compounded folders (there should be 1 file with everything directly inside it), and rename the folder "mywordpress."

6. You will want to move the "mywordpress" folder into your C drive > xampp > htdocs.

7. Then open a new tab in your browser and go to "localhost/mywordpress" then go through the steps of installing WordPress.
    - Select language
    - Click "Let's go"
    - Fill database name "mywordpress", username, and password
    - Run installation

8. Make a site title, input another username (can be same or different), same with password, your email, and install.

9. Install VSCODE or your chosen IDE to write the plug in code

### Testing

- Errors will occur on test page OR inside the test website's inspect element.

- Syntax and method errors are most common, and critical points of vulnerability that can cause errors that crash the page.

How-To:
1. Go to your MyWordPress

2. Open wp-content

3. Click on plugin

4. Paste your code folder

5. Activate your new plugin on the website

6. Run relevant shortcodes

7. Check the page for errors

8. Return to code and troubleshoot bugs if needed

9. Once passing, zip the code folder and upload to the staging site

10. Check the page for errors once again

11. Once passing, deploy to main site

