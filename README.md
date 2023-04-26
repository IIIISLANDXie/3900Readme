# **Software Installation and Usage Restrictions**

## **Virtual Machine**

1. Installing a virtual machine: [HERE](https://sourceforge.net/projects/linuxvmimages/files/VMware/L/lubuntu_20.04.1_VM.zip/download)
2. Installing virtualbox: [HERE](https://www.virtualbox.org/wiki/Download_Old_Builds_6_1)
3. Click on import:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_1.png" alt="Your image description" style="width:600px">
       </p>
4. Unzip the downloaded zip as follows:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_2.png" alt="Your image description" style="width:600px">
       </p>
5. Import the <code>lubuntu_20.04.1_VM_LinuxVMImages.ovf</code> file under this file path, set all options to default, and start.
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_3.png" alt="Your image description" style="width:600px">
       </p>
6. Enter the password: <code>lubuntu</code> and go to the desktop.
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_4.png" alt="Your image description" style="width:600px">
       </p>

## **Download Chrome**

1. First update the package list to ensure you can install the latest packages.
       <p align="center">
           <code>sudo apt update</code>
       </p>
   To install chrome (using the chrome launcher front-end), enter the command:
       <p align="center">
           <code>wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb</code>
       </p>
   Download the latest stable version of Google Chrome. Download the .deb package for 64-bit systems from the official Google repository using the following command:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_5.png" alt="Your image description" style="width:600px">
       </p>
2. Use the dpkg command to install the downloaded .deb package and enter the password <code>lubuntu</code>:
       <p align="center">
           <code>sudo dpkg -i google-chrome-stable_current_amd64.deb</code>
       </p>
   If you encounter dependencies during the installation process, you can use the following command to automatically install the required dependency packages:
       <p align="center">
           <code>sudo apt --fix-broken install</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_6.png" alt="Your image description" style="width:600px">
       </p>
3. Use command:
       <p align="center">
           <code>google-chrome</code>
       </p>
   Test for successful installation:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_7.png" alt="Your image description" style="width:600px">
       </p>

## **Download Datagrip**

1. Download the latest stable version of Datagrip using the following command:
       <p align="center">
           <code>sudo snap install datagrip --classic</code>
       </p>
       Then terimal should be:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_23.png" alt="Your image description" style="width:600px">
       </p>
2. Install Datagrip:
       <p align="center">
           <code>   datagrip   </code>
       </p>
       Then terimal should be:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_24.png" alt="Your image description" style="width:600px">
       </p>
       Install as the way you like, then log in a account (new user has 30days free trial).
       Or you can login with username <code>1435160838@qq.com</code> and password <code>Caonilaolao123</code>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_25.png" alt="Your image description" style="width:600px">
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_26.png" alt="Your image description" style="width:600px">
       </p>
3. Setup for datagrip
       After you create a new project in Datagrip, you will get into this page:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_27.png" alt="Your image description" style="width:600px">
       </p>
       Click following options:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_28.png" alt="Your image description" style="width:600px">
       </p>
       For the first time you connect database, you should download missing files for Datagrip:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_29.png" alt="Your image description" style="width:600px">
       </p>
       After that, you can click test connect and you can see successful message pop up:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_30.png" alt="Your image description" style="width:600px">
       </p>
       Click Run SQL Script and find our script from <code>capstone-project-3900w18bclavier/SQLSetup/bank_acc.sql</code>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_31.png" alt="Your image description" style="width:600px">
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_32.png" alt="Your image description" style="width:600px">
       </p>
       Then it should successfully create:
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_33.png" alt="Your image description" style="width:600px">
       </p>
       To make it easy to test, we recommend that you modify the now date in listen.py directly when testing daily payments. When testing status changes such as order completion, modify the database directly and commit (due to the nature of the group code these operations do not require a restart of the back-end server).

## **Set Dynamic Resolution**

1. Setting a dynamic resolution for a virtual machine
   Download the optimisation plugin (as the version of virtualbox to which the supplied guide is directed is 6.1.42):
       <http://download.virtualbox.org/virtualbox/6.1.42>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_8.png" alt="Your image description" style="width:600px">
       </p>
   In the VirtualBox menu bar, select your virtual machine, choose "Settings" , select "Storage" and choose "Create a virtual disc":
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_9.png" alt="Your image description" style="width:600px">
       </p>
   In the pop-up window, select "Register" and then browse to the VBoxGuestAdditions_6.1.42.iso file that you downloaded. Once you have selected the file, click on "Open" and click on "Select":
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_10.png" alt="Your image description" style="width:600px">
       </p>
   In the virtual machine, open a terminal and install the dependency packages in order to build and install Guest Additions correctly:
       <p align="center">
           <code>sudo apt install build-essential dkms linux-headers-$(uname -r)</code>
       </p>
       Go to the directory of the virtual CD. The disc will be automatically mounted in a subdirectory under <code>/media</code>:
       <p align="center">
           <code>cd /media/lubuntu/VBox_GAs_6.1.42</code>
       </p>
       Run the Guest Additions installation script with administrator privileges:
       <p align="center">
           <code>sudo ./VBoxLinuxAdditions.run</code>
       </p>
       Once the installation is complete, restart the virtual machine:
       <p align="center">
           <code>sudo reboot</code>
       </p>

# **Virtual machine environment configuration with the required libraries and MySQL configuration for the project**

1. Create the folder COMP3900 and extract the contents of the project in the folder COMP3900 for later steps.
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_11.png" alt="Your image description" style="width:600px">
       </p>

2. Open a terminal, type sudo su to switch to administrator mode (enter the password lubuntu again) and check the python3 version and pip3 version. If pip3 is not installed, first type:
       <p align="center">
           <code>sudo apt update</code>
       </p>
   Have updated the package list to ensure you can install the latest packages, then run the following command to install pip3:
       <p align="center">
           <code>sudo apt install python3-pip</code>
       </p>
   Once installed, you can use the pip3 command to install and manage all the modules.
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_12.png" alt="Your image description" style="width:600px">
       </p>

3. TYPE follow command to install all the extensions required by project:
       <p align="center">
           <code>pip3 install -r requirements.txt</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_13.png" alt="Your image description" style="width:600px">
       </p>

4. After installing all the libraries required for the project, you need to configure mysql for the virtual machine. install the MySQL server and client:
       <p align="center">
           <code>sudo apt install mysql-server mysql-client</code>
       </p>
   During the installation process, the user may be prompted to set a password for the MySQL root user. This can be set to lubuntu.
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_14.png" alt="Your image description" style="width:600px">
       </p>

5. After successful installation, enter following command to start mysql:
       <p align="center">
           <code>sudo systemctl start mysql</code>
       </p>
   Enter following command set the MySQL service to start itself at boot:
       <p align="center">
           <code>sudo systemctl enable mysql</code>
       </p>
   Enter following command ensure that the MySQL service is up and running, you can check its status:
       <p align="center">
           <code>sudo systemctl status mysql</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_15.png" alt="Your image description" style="width:600px">
       </p>

6. After ensuring that mysql has been started, enter the following command to try to connect to mysql::
       <p align="center">
           <code>mysql -u root -p</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_16.png" alt="Your image description" style="width:600px">
       </p>

7. Create database:
       <p align="center">
           <code>create database car_space</code>
       </p>
   Use this database:
       <p align="center">
           <code>USE mysql;</code>
       </p>
   Change the authentication plugin for the root user. This will allow the user to authenticate with a password:
       <p align="center">
           <code>ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'lubuntu';</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_17.png" alt="Your image description" style="width:600px">
       </p>

8. Refresh privileges:
       <p align="center">
           <code>FLUSH PRIVILEGES;</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_18.png" alt="Your image description" style="width:600px">
       </p>

9. Exit mysql:
       <p align="center">
           <code>   exit;   </code>
       </p>
   Restart mysql:
       <p align="center">
           <code>sudo systemctl restart mysql</code>
       </p>
       <p align="center">
           <img src="VirtualBoxSetup/virtualBox_19.png" alt="Your image description" style="width:600px">
       </p>

10. Start the back-end server:
        <p align="center">
            <code>python3 -m src.backend.main</code>
        </p>
    You will see a message that the backend has been started, which means that the server was started successfully. Please note! Please note! Please note! You must make sure that <code>MYSQL_PASSWORD: str = lubuntu</code> is in <code>src/backend/config</code>. You can start using and testing our project by double clicking on <code>login.html</code> to open the login screen.
        <p align="center">
            <img src="VirtualBoxSetup/virtualBox_20.png" alt="Your image description" style="width:600px">
        </p>
        <p align="center">
            <img src="VirtualBoxSetup/virtualBox_21.png" alt="Your image description" style="width:600px">
        </p>

11. It is worth noting that the full start of the server requires waiting for all registers to be started. In order to print the output for completeness, I have each thread wait 1 second after the previous thread has started before starting (this is not an inefficient algorithm causing the delay). After seeing that all four INFOs have been printed, the server can be stopped by "CTRL C". Please note that some threads (such as updating low demand spaces) will start once at the start of the server, but the next one will start much later (7 days or 4 months or more). This is to simulate the effect of a real car rental page. (select chrome launch)
        <p align="center">
            <img src="VirtualBoxSetup/virtualBox_22.png" alt="Your image description" style="width:600px">
        </p>

12. For the tests, we use postman to simulate the addition and manipulation of data (as the results of each execution of the pytest test are not visual enough). This is the interface documentation for postman, which covers the manipulation of interface data for almost all routers. Each time a new route is implemented, we perform unit and integration tests for every conceivable scenario of this route.

    <p align="center">
        <code>https://app.getpostman.com/join-team?invite_code=feb6aaeae7c108d364f7bf81d68dac5a&target_code=139283ac86e729a5e1886abf73e2a2b8</code>
    </p>

13. Considering that the test required the server to create multiple spaces before the recommended spaces could be seen, you need to create multiple car space in database.
