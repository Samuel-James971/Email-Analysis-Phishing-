# Email-Analysis-Phishing-
This project focuses on the detection and analysis of phishing emails through a multi-layered approach involving URL inspection, email header analysis, and the deployment of an email filtering tool. The goal is to identify malicious indicators, understand phishing tactics, and enhance email security protocols within an organization.

<br />

<h2>Project walk-through:</h2>

<p align="center">
Head to the github repository phishing pot, here is a curated collection of real phishing email samples that have been captured through honeypots: <br/>

![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-09%20094109.pdf.png?raw=true)
<br />
<br />
For this project download a few of the sample phishing emails, however make sure this is done inside a VM for safety purposes:  <br/>
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20141747.png?raw=true)
<br />
<br />
For this project I will be using Bitdefender Security as it has an email protection feature: <br/>
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20142236.png?raw=true)
<br />
<br />
I have sent some of the phishing emails to the email account that I have paired with Bitdefender:   <br/>
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20161240.png?raw=true)
<br />
<br />
As you can see Bitdefender has flagged these emails as dangerous, in a real world context, it would be our responsibility to conduct an analysis of these messages to identify any suspicious content:  <br/>
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20161240.png?raw=true)
<br />
<br />
One method of identifying suspicious content is through URL analysis. In this case, the URL embedded in the email (cradletool.com) does not align with the sender, which references a Hulu membership. This mismatch is a strong indicator of potential phishing activity. :  <br/>
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20161352.png?raw=true)
<br />
<br />
Further analysis can be done on the URL using symantec sitereview, this shows that the URL is categorized as a security risk:
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20161352.png?raw=true)
<br />
<br />
By opening the email in a text editor, the Return Path field becomes visible within the header information. In this instance, the Return Path does not correspond with the display name of the sender, which is a common red flag indicating suspicous activity:
![image alt](https://github.com/Samuel-James971/AI-Workflow-Automation/blob/main/Screenshot%202025-07-08%20161352.png?raw=true)
<br />
<br />
This method also allows for the identification of the sender’s IP address within the email headers. By cross referencing the IP using two reputable IP lookup services, I found that the address had not been previously reported for malicious activity. However, based on the other indicators such as mismatched URLs and inconsistent Return Path data it can confidently concluded that these emails are suspicious and should not be opened: 

![image alt](https://github.com/Samuel-James971/Email-Analysis-Phishing-/blob/main/Screenshot%202025-07-16%20223208.png?raw=true)
![image alt](https://github.com/Samuel-James971/Email-Analysis-Phishing-/blob/main/Screenshot%202025-07-16%20223419.png?raw=true)
![image alt](https://github.com/Samuel-James971/Email-Analysis-Phishing-/blob/main/Screenshot%202025-07-16%20223153.png?raw=true)



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
