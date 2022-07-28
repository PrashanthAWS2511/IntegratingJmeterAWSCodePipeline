














**Integrating Load Test(Jmeter Script) With Blazemeter In AWS CICD Pipeline**



|**Version**|**Author**|**Created Date**|
| :- | :- | :- |
|1.0|Prashanth Mudaliar|28-July-2022|































Index


|**Steps**|
| :- |
|Step 1: Creating Jmeter Script for Load Test|
|Step 2: Integrating the Jmeter script in Code Pipeline|







































**Prerequisites:**

- A Web API For Testing
- A CICD pipeline to integrate Load Test Stage
- Jmeter
- JDK














































**Step 1**: **Creating Jmeter Script for Load Test**

i. Launch Jmeter by clicking on Jmeter.bat file

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.001.png)



`		`![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.002.png)






ii. Add new **Thread Group** to the **Test Plan**

Right Click on **Test Plan** -> **Add** -> **Threads (Users)** -> **Thread Group**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.003.png)

iii. Edit the **Thread Group** Details as shown below

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.004.png)










iv. Right Click on **Thread Group** -> **Add** -> **Sampler** -> **Http Request**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.005.png)

v. Edit the **Http Request** as shown below

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.006.png)







vi. Save the **Test Plan**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.007.png)













**Step 2**: **Integrating the Jmeter script in Code Pipeline**

i. Edit the Pipeline in which you want to integrate Load Test Stage

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.008.png)

ii. Click on **Add Stage**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.009.png)

iii. Enter the **Name** of stage and click on **Add Stage**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.010.png)

iv. Click On **Add action group**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.011.png)
















v. Enter/ Select the details as shown below and Click on **Connect to BlazeMeter**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.012.png)





















vi. A popup window will open asking **BlazeMeter Credentials** if you don’t have one create and log into Blazemeter

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.013.png)

vii. After Login go to **Performance** tab and click on **Create Test**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.014.png)



viii. Edit the test name, upload the script and load configuration details as shown below

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.015.png)

ix. Scroll down and you can set the **Failure Criteria** as shown below (optional)

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.016.png)

x. After all the changes click on **Save & Connect**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.017.png)

xi. You Will be redirected to **AWS** page for **Processing OAuth request** click on **Confirm**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.018.png)

xii. The popup will be closed and you can see a **Success** message on **AWS** page, click on **Done**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.019.png)

xiii. Click on **Done**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.020.png)

xiv. Scroll up and Click on **Save**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.021.png)






xv. Run the Pipeline by committing the changes and check the Load Test Report

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.022.png)

xvi. Blazemeter Screen

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.023.png)


