














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

1. Launch Jmeter by clicking on Jmeter.bat file

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.001.png)



`		`![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.002.png)






1. Add new **Thread Group** to the **Test Plan**

Right Click on **Test Plan** -> **Add** -> **Threads (Users)** -> **Thread Group**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.003.png)

1. Edit the **Thread Group** Details as shown below

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.004.png)










1. Right Click on **Thread Group** -> **Add** -> **Sampler** -> **Http Request**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.005.png)

1. Edit the **Http Request** as shown below

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.006.png)







1. Save the **Test Plan**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.007.png)













**Step 2**: **Integrating the Jmeter script in Code Pipeline**

1. Edit the Pipeline in which you want to integrate Load Test Stage

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.008.png)

1. Click on **Add Stage**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.009.png)

1. Enter the **Name** of stage and click on **Add Stage**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.010.png)

1. Click On **Add action group**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.011.png)
















1. Enter/ Select the details as shown below and Click on **Connect to BlazeMeter**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.012.png)





















1. A popup window will open asking **BlazeMeter Credentials** if you don’t have one create and log into Blazemeter

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.013.png)

1. After Login go to **Performance** tab and click on **Create Test**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.014.png)



1. Edit the test name, upload the script and load configuration details as shown below

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.015.png)

1. Scroll down and you can set the **Failure Criteria** as shown below (optional)

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.016.png)

1. After all the changes click on **Save & Connect**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.017.png)

1. You Will be redirected to **AWS** page for **Processing OAuth request** click on **Confirm**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.018.png)

1. The popup will be closed and you can see a **Success** message on **AWS** page, click on **Done**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.019.png)

1. Click on **Done**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.020.png)

1. Scroll up and Click on **Save**

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.021.png)






1. Run the Pipeline by committing the changes and check the Load Test Report

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.022.png)

1. Blazemeter Screen

![](Images/Aspose.Words.57a182b4-25d6-4355-887c-d0d1983a30a5.023.png)


