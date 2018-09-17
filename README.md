# Moodle-HDM-Plugin
On this readme I will describe the full tutorial of how to install moodle and then how to install the custome plugin on it.

## Installation

### 1) Linux VM Installation
In order to continue to the Moodle Installation. You should have Linux OS.
I used ubuntu 18.04 running on VMWare Workstation and the Moodle installation works perfect with out any error.  
VMware [download here](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html)  
Ubuntu 18.04 [download here](https://www.ubuntu.com/download/desktop/thank-you?country=IL&version=18.04.1&architecture=amd64)


### 2) Moodle Installation
After you installed your Ubuntu os on the VM, you are allows to continue to the Moodle installation.
I found a perfect installation instractions at: https://websiteforstudents.com/setup-moodle-cms-on-ubuntu-18-04-lts-beta-with-apache2-mariadb-and-php-7-1-support/  
Please follow every instaction very carefully and it should work.   
In order to check if everythoing is work fine, try to brows to "localhost" - if you see the Moodle installation appear in your browser so you in the right way.

### 3) Plugin Installation(finally!)
I originally based my plugin on the template that I found here: https://github.com/moodlehq/moodle-mod_newmodule.  
On this template repository their is instractions of how exectlly you add your own plugin to moodle. BUT I will give you here only the *relevant* and *short* instactions to install this plugin on your own Moodle System.

#### Instractions:
1. Clone this repository into a tmporary folder.
2. From the cloned folder, copy the "hdm" folder and paste it into /mod folder of the moodle directory.(you should find this directory at: `/var/www/html/moodle/mod`).  
3. Visit Settings > Site Administration > Notifications, you should find the module's tables successfully created.    
4. Go to Site Administration > Plugins > Activity modules > Manage activities and you should find that this newmodule has been added to the list of installed modules.  
5. You may now proceed to run your own code in an attempt to develop your module. You will probably want to modify mod_form.php and view.php as a first step. Check db/access.php to add capabilities. Go to Settings > Site Administration > Development > XMLDB editor and modify the module's tables.

#### *How to check if everything is work fine?*
1. Create course in Moodle as Admin(you can enter as admin using the username and password you entered on the Moodle installation from stage 2.) ---> creating a course done by: Site Administration->Courses tab->Manage courses and categories->Create new course.  
2. Return to the Site Home and enter to the course OR click on "save and review" after you finish the creation of the new course.
3. Follow the next pictures:
