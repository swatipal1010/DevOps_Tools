## Basic build pipeline with integration of Maven
1. Keep a copy of any Java project in the github repository. In my case, I am going to use https://github.com/swatipal1010/time-tracker_Maven_Project.git project.
2. Login to your Jenkins account.
3. In the dashbaord of Jenkins follow these steps to integrate Maven with Jenkins :
   - First install the **Maven Integration** plugin
     a. Go to **Manage Jenkins** section from LHS in dashboard.
     
     ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/1b15a419-fd79-44ed-b681-dd7073eb3ca4)
     
     b. Click on **Plugins** option present under **System Configuration**

     ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/be107a57-e2f8-495b-919e-f8dd0734869d)
     c. In the search box that appears after clicking on **Available Plugins**, search for **Maven Integration** plugin. (Since I have laready installed this plugin, I can get this under **Installed plugin**)
     
     ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/c143737e-a0f1-4222-8a72-a93af1506fb1)

   - Now add the JDK and Maven to **Global System Configuration** so that Jenkins can use Maven to uild the java project using the JDK and Maven present in the local machine.
     a. Go to **Manage Jenkins** -> **System Configuration** -> **Tools** 
     
     ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/56936ec0-68cb-4388-b690-f249aab24988)
     b. Under **JDK Installations**, do the following:
        **Add JDK** -> **Name**(any name of your choise** -> **JAVA_HOME**(Location of jdk in your local machine) -> Uncheck **Install automatically** option if the JDK is already installed in the local machine.
     
     ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/55ddbbb0-b199-4788-844d-c375a9c4ecbe)
     
     c. Under **Maven Installations** -> **Add Maven** -> **Name**(anything ofyour choise) -> **MAVEN_HOME**(add the path to maven installation in your system) -> Uncheck the **install automatically** option if the MAVEN is already installed in the system.

     ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/a8107030-a4c1-4a3d-966d-64d66537ecfb)
     
     d. Click on **Apply** -> **Save** or directly on Save(to return to Dashboard directly).
4. To build the pipeline, click on **New Item** in LHS of Jenkins dashboard.
5. **Enter an item name**
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/ce48c108-8123-4065-a18c-d009de711f83)

6. Select **Maven Project** Option.
7. Click on **OK**
8. In **Source Code Management**, click on **Git** -> **Repositories** -> **Repositories URL**
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/a83ed0e2-731c-473d-bed2-dbf8bfb56521)

9. Under **Build** -> **Goals and Options** -> **clean package**
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/4ec2ced5-e146-4e73-89cf-a43ce64a082d)

10. Click on **Save**
11. To run the pipeline, follow these steps:
    a. Go to dashboard, and click on the drop-down arrow against the name of the job
    ![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/2654942b-4970-4bb6-8c25-f336c4e6ddde)

12. Click on **Build Now** and you can see the pipleine build getting executing
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/7fabed38-7dd5-46e8-b032-f775ee42debd)

13.We can see the status of build (Red and cross - Failed pipeline, Green and check - Success)
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/c5f10b9f-5a5d-45b6-81bb-0b0dbf9b5fc5)

14. We can also see the console Output by clicking on the build and then onn **Console Output**
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/df8a717b-ebaa-4969-b682-2f69bf6db3f4)

![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/b3021bdd-d869-41f5-990a-546bc1487644)








   


