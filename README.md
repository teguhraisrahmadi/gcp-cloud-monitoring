# Google Cloud Platform

## Work Instruction for Using Cloud Monitoring

1. Before we run cloud project, we need create VM which will be monitored.  
<br> ![Capture](Material/1.png) <br>

2. Then connect to the vm, and run web server (I am using apache web server).
   Run this command :
   “sudo apt-get install apache2”
<br> ![Capture](Material/2.png) <br>

3. Run this command for install agent to the vm :
   “curl -sSO https://dl.google.com/cloudagents/install-monitoring-agent.sh”
<br> ![Capture](Material/3.png) <br>

   “sudo bash install-monitoring-agent.sh”
<br> ![Capture](Material/4.png) <br>

4. Run this command for install cloud log to the vm :
   “curl -sSO https://dl.google.com/cloudagents/install-logging-agent.sh”
   “sudo bash install-logging-agent.sh –structured”
<br> ![Capture](Material/5.png) <br>

5. The we configure the Cloud Monitoring.
   Go to App Cloud Monitoring menu, and choose Metrics Scope. 
<br> ![Capture](Material/6.png) <br>

6. This view mean, your project was detected by cloud monitoring. But if you want add another project to monitor, you can click “Add Cloud Projects to metrics scope”.
<br> ![Capture](Material/7.png) <br>

Create Uptime Check and Alert.

7. Go to uptime check menu.
<br> ![Capture](Material/8.png) <br>

8. Then create uptime check.
<br> ![Capture](Material/9.png) <br>

9. Fill the title, etc as you want, but you can follow this option.

10. Title.
<br> ![Capture](Material/10.png) <br>

11. Terget
<br> ![Capture](Material/11.png) <br>

12. Response Validation
<br> ![Capture](Material/12.png) <br>

13. Alert & Notification. 
    Click manage notification channel. New tab will be opened.
 <br> ![Capture](Material/13.png) <br>

14. Choose email and click add new (you can choose other than email)
 <br> ![Capture](Material/14.png) <br>

15. Fill your email and display name what you want. Then click save.
<br> ![Capture](Material/15.png) <br>

16. Go back to uptime check menu, and click refresh.
<br> ![Capture](Material/16.png) <br>

17. You can see, the channel was displayed, then choose that and click ok.
<br> ![Capture](Material/17.png) <br>

18. After that, we test the check.
<br> ![Capture](Material/18.png) <br>

19. If the respond is “200” it mean test be succeed. Then click create.
<br> ![Capture](Material/19.png) <br>

20. Wait a few minutes, until uptime check success to be created. Uptime check was created.
<br> ![Capture](Material/20.png) <br>
<br> ![Capture](Material/21.png) <br>

Simulation Condition if your VM gonna be stop.

21. Go to compute engine and stop the vm.
<br> ![Capture](Material/22.png) <br>

22. You will be receive the alert email notification that your vm stoped. Check your email.
<br> ![Capture](Material/23.png) <br>

Simulation Condition if your VM gonna be startup again.

23. Go to compute engine and start the vm.
<br> ![Capture](Material/24.png) <br>

24. You will be received the alert email notification that your vm is running. Check your email.
<br> ![Capture](Material/25.png) <br>

Custom your dashboard and charts.

25. Go to cloud monitoring dashboard menu and click create dashboard.
<br> ![Capture](Material/26.png) <br>

26. Follow the instruction, and fill what you want.

27. Name
<br> ![Capture](Material/27.png) <br>

28. Chart
<br> ![Capture](Material/28.png) <br>

29. You can choose your chart you want. I am using line for this.
<br> ![Capture](Material/29.png) <br>

30. You can choose any option for resource monitoring. For this I am using cpu utilization for display mean cpu utilization with 1 minute interval.
<br> ![Capture](Material/30.png) <br>

31. You can add another matric, just click it.
<br> ![Capture](Material/31.png) <br>

32. I add another metric for display disk read byte.
<br> ![Capture](Material/32.png) <br>

33. Done, Thanks.
