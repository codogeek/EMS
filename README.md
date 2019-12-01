How to run the Entry Management System Project -

1. Download the zip file.

2. Extract the file and copy ems folder.

3. Paste inside root directory(for xampp xampp/htdocs, for wamp wamp/www, for lamp var/www/html).

4. Open PHPMyAdmin (http://localhost/phpmyadmin).

5. Create a database with name ems.

6. Import ems.sql file(given inside the zip package in SQL file folder).

7. Run the script http://localhost/ems_index.php.

Credential for admin panel :

Username: admin 
Password: admin@9


In order to send emails and sms, follow the following steps - 

1. Go to C:\xampp\sendmail\sendmail.ini and edit it.

2. Update smtp_server to your mail id and smtp_port to 465. smtp server for yahoo account is smtp.mail.yahoo.com and for gmail is smtp.gmail.com. These both run on SSl so change smtp_ssl to ssl.

3. Now put your email id and password in auth_username and auth_password.

4. Go and save this file.

5. Now go to another file C:\xampp\php\php.ini and edit it.

6. When you search for sendmail, it will take you to mail function. Comment out the following statements - SMTP=localhost  and smtp_port=25

7. Remove the semicolon from the statement sendmail_from and add your mail id here.

8. Remove the semicolon from the statement sendmail_path and add the path. For me, it's "C:\xampp\sendmail\sendmail.exe -t"

9. Go and save this file.

10. for this to take effect, you need to restart Apache in xampp.

11. Make sure to turn on the "Allow less secured apps to send mail" feature in the settings of your email account.


Description -

When you'll run the ems_index.php, admin login box will show up. Enter the admin credentials provided above to access the entry management system.
Once accessed granted, it will take you to the home page where you will find the menu bar and description of the application.
To register the visitor, go to Add new visitor tab, a form will show up, add the details and submit the form. As soon as you submit the form, on verifying the details, the software will trigger a mail to the host with visitor's details. The code for the same can be found in ems_add_new_visitor.php file.
To add the checkout time of the visitor, go to Manage visitors tab in the menu, a form will show up, add the details and submit the form. As soon as you submit the form, on verifying the details, the software will trigger a mail to the visitor regarding the details of the meeting. The code for the same can be found in ems_manage_visitors.php file.
To logout of the software, go to logout tab in the menu.
