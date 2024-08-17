![image](https://github.com/user-attachments/assets/da9dd89a-908a-46be-8c2c-c74425eaf766)



<h1></h1>
This tutorial outlines the implementation Os ticket, including creating users managing SLA and working open tickets.<br />

<p>
  Welcome to this tutorial on Os Ticket, a robust and widely-used open-source support ticket system. Os Ticket streamlines customer support by managing, organizing, and archiving support requests in one central location. Whether you’re a small business or a large organization, Os Ticket provides the tools necessary to efficiently handle customer inquiries, ensuring timely and effective resolution.

In this tutorial, we’ll guide you through the essential features of Os Ticket. You’ll learn how to set up agents and users, define and manage Service Level Agreements (SLA) to ensure prompt responses, and efficiently handle and close tickets. By the end of this tutorial, you’ll have the knowledge to optimize your support system for better customer service and operational efficiency.
</p>




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Os Ticket

<h2>Operating Systems Used </h2>
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Configure roles
- Configure teams
- Configure agents
- Creation of users and allowing them to create tickets
- Configuration of SLA and help topics

<h2>Deployment and Configuration Steps</h2>
<p>
To begin, we will start configuring our settings starting with the roles of our admin. Notice that we have two different panels within Os Ticket. The admin panel is where a SysAdmin is able toperform activities like configuration and management of  the ticket system and creatation of agents Service Level Agreements, and teams. The agent panel is for ticket handling and customer interaction. 
</p>
<br />

<p>
  Once we login in to our account as an admin we can begin configuration by first navigating to our admin panel. In this step we are going to create a 'Chief Admin' role with the power to manage and configure anything within our site. To create a new role named 'Chief Admin' within the Admin Panel of Os Ticket, navigate to the Admin Panel, then click on the Agents tab, and select Roles from the dropdown menu. Here, you'll see a list of existing roles. Click on the Add New Role button, and a form will appear where you can input the name of the new role—enter 'Chief Admin.' Next, define the permissions for this role by selecting the appropriate checkboxes for each administrative function that the Chief Admin should have access to. Once all settings are configured, click Save Changes to finalize the creation of the new role. This role can now be assigned to any agent as needed.
</p>
<br />

![chiefadminsetup](https://github.com/user-attachments/assets/cbc307b0-dfff-44c3-86ae-6667a650e210)

<br />
<P>Note: Be sure that all desired permissions are checke off before clicking the 'add role' button.</P>

<br />

![chiefadmin_roles1](https://github.com/user-attachments/assets/510f0615-51c2-4a7a-9f09-e81e8df7321b)

<p>
For our next step we will create a few departments that we will be assigned different tickets depending on the nature of the issue involved. Once again this will be accomplished within the Admin Panel.
</p>
<p>Access the Admin Panel and navigate to the Agents tab. From the dropdown menu, select Departments note that there are two default departments that exist already: 'Maintenance' and 'Support'.
</p>
<br />

![image](https://github.com/user-attachments/assets/b2596cd7-d14b-4e99-aafd-941c3b9c39ff)




<p> Continue by clicking on the Add New Department button. In the form that appears, enter 'System Administrators' as the department name and configure any additional settings as needed, such as assigning a manager or setting department-specific permissions. Once you've configured the necessary options, click Save Changes to create the new department. This department can now be assigned to agents to organize and manage tickets effectively. </p>
<br />


![image](https://github.com/user-attachments/assets/35b915a1-82a6-4cbf-87fe-5ab0080377cc)

<br />

<p>
Next we will set up our teams in which we can organize our agents and assign SLA topics in the coming steps. In Os Ticket, Teams are used to group agents with specific skills or responsibilities, enabling more efficient ticket management and collaboration. Unlike departments, which typically organize agents by their role in the organization (e.g., IT, Billing), teams allow you to bring together agents from different departments to work on particular types of tickets or projects.
</p>
<p>We will create two new teams named Level I support and Level II suport.To create two teams in Os Ticket named 'Level I Support' and 'Level II Support,' start by accessing the Admin Panel and navigating to the Agents tab. From the dropdown menu, select Teams and click on the Add New Team button. For the first team, enter 'Level I Support'. Configure any additional settings, such as team permissions, and then click Save Changes. Repeat this process to create the 'Level II Support' team, we will assign the appropriate agents and configure the settings in a later step. These teams can now be used to manage and assign tickets based on the support level required. </p>
<br />

![level2supp_team](https://github.com/user-attachments/assets/9f2b5f38-7912-4282-803e-8d72ab55b667)

<br />

<p> To create two new agents named Jenny and John in Os Ticket, first, access the Admin Panel and navigate to the Agents tab. Click on Add New Agent and fill in the required information for Jenny, such as her name, email address, and username. Assign her to the appropriate department, role, and team if needed, then set a password for her account. Once done, click Create to finalize her agent account. Repeat this process for John by entering his details and assigning the necessary roles and permissions. Both agents, Jenny and John, will now be able to log in and manage tickets based on their assigned roles and departments.</p>

<br />

<p> Next we will create some new agents in order to work tickets from our users. To create two new agents named Jenny and John in Os Ticket, first, access the Admin Panel and navigate to the Agents tab. Click on Add New Agent and fill in the required information for Jenny, such as her name, email address, and username. At this time I will assign her as a Lead in the  Systems Administrators department we just created and also add her to the Level I support team since that will be serving as a team for our subject matter experts. Once done, click Create to finalize her agent account. Repeat this process for John by entering his details and assigning John to the Support Department and the Level II support team. Both agents, Jenny and John, will now be able to log in and manage tickets based on their assigned roles and departments.</p>

<br />

![agentjenny1](https://github.com/user-attachments/assets/f62180e6-5b00-4af6-a736-67a12fea5a6f)

<br />

<p> (below) John's access rights setup</p>

<br />

![image](https://github.com/user-attachments/assets/237ea23e-e121-41d3-af9d-ed1469b66635)
<br />

<p> For our next configuration step we are going to set up our SLA. In Os Ticket and other ticketing systems, a Service Level Agreement (SLA) is a set of predefined rules that outline the expected response and resolution times for handling support tickets. SLAs help ensure that customer inquiries are addressed within a specific timeframe, maintaining service quality and meeting customer expectations. They can be configured based on various criteria, such as ticket priority, issue type, or customer status. For instance, high-priority tickets might have shorter response times compared to low-priority ones. SLAs are essential for managing customer satisfaction and keeping support teams accountable for timely issue resolution. </p>

<p> For our exercise we will create three SLA categories: Sev_A, Sev_B, and Sev_C. Sev_A will have tickets with the most severe issues like a website crashing or other obstacles to normal business functions. To set up the three SLA levels in Os Ticket, start by navigating to the Admin Panel and selecting Manage from the SLAs tab. Click Add New SLA Plan to create the first level, 'Sev-A,' and set the grace period to one hour. Under the schedule settings, choose the 24/7 option to ensure that this SLA applies at all times.  </p>

<br />

![SLAsetupA](https://github.com/user-attachments/assets/fa02d9b4-4350-4c4a-9757-7cb8779eb704)
<br />

<p> Next, create the 'Sev-B' SLA by repeating the process, setting the grace period to four hours, and selecting the 24/5 schedule, which covers Monday through Friday. Sev-B will involve any issues that are not an immediate emergency but still present a significant obstacle to daily business for our hypothetical business.</p>

<br /> 

![SLAsetupB](https://github.com/user-attachments/assets/3ef5e4c4-bf66-4518-a9fc-13d79a958f2d)
<br />

<p> Finally, for 'Sev-C,' set the grace period to eight hours, and configure the schedule to Monday-Friday from 8 a.m. to 5 p.m., excluding U.S. holidays. Save each SLA plan after configuring its settings, and they will be ready for use in managing ticket response times. Again, for our fictional company, Sev-C tickets will include issues that are of a minor importance and do not hinder employees from accomplishing their daily tasks. </p>


<br />

![SLAsetupC](https://github.com/user-attachments/assets/faa0ecc9-72bd-4019-bcbc-32c0058788dd)
<br />

<p> For our last item we will cover the Help Topics.In Os Ticket, Help Topics are predefined categories that guide users when submitting support tickets, helping them accurately describe their issue or request. By selecting a relevant help topic from a dropdown menu, users can categorize their tickets, ensuring they are routed to the appropriate department or team for resolution. Help Topics streamline the ticketing process by enabling more efficient ticket triage, assignment, and prioritization, ultimately improving response times and ensuring that issues are handled by the most qualified agents. They are essential for organizing support requests and ensuring that each ticket receives the appropriate attention. </p>

<p> To create the help topic categories in Os Ticket, such as 'Business Critical Outage,' 'Personal Computer Issues,' 'Equipment Request,' and 'Password Reset,' start by accessing the Admin Panel and navigating to the Manage tab, then select Help Topics from the dropdown menu. Click on Add New Help Topic to create the first category, 'Business Critical Outage.' Enter the name and configure any necessary settings, such as assigning it to a specific department or SLA. Repeat this process for the other categories: 'Personal Computer Issues,' 'Equipment Request,' and 'Password Reset.' Each help topic will now be available for users to select when submitting a ticket, ensuring their requests are properly categorized and directed. </p>

<br />

![pcissues_helptopic](https://github.com/user-attachments/assets/d81ecdf2-7006-48f6-b7db-e840d4f372b0)
<br />


<p> In conclusion, this tutorial has guided you through the essential configurations of the Os Ticket system, including adding agents, setting up departments, defining Service Level Agreements (SLAs), and creating help topics. By following these steps, you've laid a solid foundation for an effective ticketing system that enhances customer support operations. In the next tutorial, we will delve into managing tickets and documentation within Os Ticket, where you will learn how to effectively handle incoming requests, track ticket progress, and maintain comprehensive records to ensure efficient support workflows. Thank you for joining me, and I look forward to seeing you in the next session!</p>

