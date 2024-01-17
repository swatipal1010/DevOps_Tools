## Automating the pipeline using Schedular and Poll SCM
A. **USING SCHEDULAR**
1. Create a **Maven Project** Pipleine.
2. In the configuration page, in the **Source Code Management** section, mention the repository link that conatins the project.
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/4af19993-8e7f-4090-8b40-16ab9c880790)

3. In the **Build Triggers** section, check the **Build Periodically** option. In the schedule region, mention the time after which you want yourpipeline to be executed again.
***** indiactes that the pipeline will run after every minute of each hour, each day, each month, each week.
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/07207e23-4c0a-410d-ad75-2bbf92c425a6)

4. Fill **Goals and Options** (clean package - for project using Maven) and then Click on **Save**.
5. You will see the jobs being executed one after the another after every minute.
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/7eeea3d2-2269-40ce-b2a9-6795239daaa7)

- There's a drawback of scheduling the jobs this way. The pipeline keeps on executing even if no changes are made into the project's code. Thus, we use POLL SCM method where the Jenkins will check the specified GitHub repo for changes after every fixed time interval specified for the pipeline. If on checking the repo, Jenkins found any changes made into the code, the pipeline will start executing.

B. **USING POLL SCM**
1. Create the **Maven-project pipeline**.
2. In the configurations page, mention the repo you want the pipeline to be executed for.
3. In the **Build Triggers** section, choose **Poll SCM** -> **Schedule**
![image](https://github.com/swatipal1010/DevOps_Tools/assets/110754474/1117682c-d7ed-40f6-9857-cedf65b6f11c)

4. Fill **Goals and Options** (clean package - for project using Maven) and then Click on **Save**.
5. Make some changes to the project's code and you can see the pipeline getting triggered automatically.






