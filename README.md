# osTicket2-Config-Deployment

## osTicket Lab and Tutorial 2: Configuration for Deployment

In first tutorial we went through all the steps of setting up osTicket, an online IT Helpdesk Ticketing System, on a Microsoft Azure Virtual Machine. We have set up all the necessary tools to begin using the osTicket software. The lab consisted of the following technologies: Microsoft Azure Cloud/Virtual Machines, Remote Desktop, Internet Information Services, PHP, SQL, C++, and osTicket. 

Now we are going to set up Admins and Employees/Users for our system. Make sure your Virtual Machine is up and running then use Remote Desktop Connection to log in. Open Microsoft Edge and navigate to  http://localhost/osTicket/scp/login.php.
 
![image](https://user-images.githubusercontent.com/114452968/231040001-c5afdb85-878a-4515-a6a5-86a6deabf147.png)

## Add Agents to Helpdesk

In the top right click Agent Panel > Agents >Agents > Roles. 
 
![image](https://user-images.githubusercontent.com/114452968/231040061-02891180-dbae-47b6-b858-f06286f63b73.png)
![image](https://user-images.githubusercontent.com/114452968/231040073-0349dfa3-90bd-496a-bc0c-a5fb7914e528.png)

Click Add New Role. I am calling my new role “Emperor Admin” because we are giving them all permissions when it comes to tickets. After giving Emperor Admin all permissions, we will click Add Role.
 
![image](https://user-images.githubusercontent.com/114452968/231040129-c66730d8-4e4b-4e08-baa7-24edc552d891.png)
![image](https://user-images.githubusercontent.com/114452968/231040141-bc9163e0-387f-4fe0-b308-9108c4f100e0.png)
 
Time to adjust our Departments. Click on Departments and we will add a new department called System Administrators, and they are under the Parent department: “Support.” Scroll down and click Create Dept.
 
![image](https://user-images.githubusercontent.com/114452968/231040177-9b1b96d2-4596-45fe-a0f9-0f6825b9a97c.png)

Next, we will go to our Teams in the navigation menu. Level I Support Team is already created so we are going to create Level II Support so that Level I has some backup in case tickets need to be elevated. Click Add New Team, name the team Level II Support, and click Create Team. I have gone ahead and added myself as a member of the Team Level II Support.
 
![image](https://user-images.githubusercontent.com/114452968/231040219-6294a390-60be-4097-b2cf-e2c9025d34f8.png)

Since we have our ticketing system running, we need to make sure that anyone that needs to can create a ticket. Go to Settings > Users and arrive at Users Settings. Ensure that the Registration Required box is NOT checked.
 
![image](https://user-images.githubusercontent.com/114452968/231040258-4c166f2c-cdc3-43a9-b241-f6c22c42fa46.png)

Under Agents we are going to configure our workers at Hussell Helpdesk. Click Add New Agent then fill out the name, email, and username. In the real world we would send them a link to reset their password, but for this tutorial/lab we will give them a password. My first agent is name Han Solo!
 
![image](https://user-images.githubusercontent.com/114452968/231040290-4335a5c6-45a5-4822-ae90-7b81a25c66eb.png)
![image](https://user-images.githubusercontent.com/114452968/231040312-ad7e99f8-6306-4061-a2a7-066d8562522b.png)
 
Let’s get Han set up to manage tickets. Go to the Access tab and put Han in the Support/System Administrators Department, give him the role of Emperor Admin, then click create.

![image](https://user-images.githubusercontent.com/114452968/231040336-2c68111c-77b7-4989-8921-5c40b7edfc83.png)
 
Let’s create another agent! Ben Kenobi has been hired and has the same Access as Han Solo. Good practice dictates that there is always more than one individual that can manage tickets in case of an emergency.
 
![image](https://user-images.githubusercontent.com/114452968/231040373-29971225-b1f6-461d-be2f-dc9f5c3c9406.png)
![image](https://user-images.githubusercontent.com/114452968/231040404-ea7b61ae-b2b6-481d-a098-483656f9d3a1.png)

Now we will begin to add employees/users. Click Agent Panel in the top right > Users > Add User. Enter their email and username. Padme Skywalker is my first user. Create one more, these will be the people in our system and network that can create tickets requesting IT support. Leia Solo is next user. Now we have users that can submit tickets and different levels of Agents/employees that can service these tickets.

![image](https://user-images.githubusercontent.com/114452968/231040570-ce1533a4-2fb7-4366-b74d-6ac4f049a338.png)
 
## Service Level Agreement (SLA)

Service Level Agreements (SLA’s) are very important when it comes to a Helpdesk. SLA’s help to triage tickets that come in, so that a proper order of response can be performed.
 
![image](https://user-images.githubusercontent.com/114452968/231040637-a976517e-dcc0-4d43-a6ed-b6a7be9a872b.png)

Let’s create our SLA’s. Click Agent Panel > Manage > SLA > Add a New SLA Plan.
 
![image](https://user-images.githubusercontent.com/114452968/231040659-8ca6d76e-582c-4e0f-8a53-9ae062e9f3fe.png)

For this tutorial we will make three levels of SLA:
-Severity-1: 1 hour, 24/7
-Severity-2: 4 hours, 24/7
-Severity-3: 8 hours, business hours
 
![image](https://user-images.githubusercontent.com/114452968/231040698-5d6ffddf-0925-41e8-9ce6-e793982ca000.png)
![image](https://user-images.githubusercontent.com/114452968/231040726-c694c91d-c2a0-45eb-aea7-512124e17531.png)
 
When users submit a ticket to our Helpdesk, we need to have some categories or topics under which we put those tickets. We will create four categories that correspond to some common issues that users may experience. Do not confuse this with SLAs, as these are merely topics that can have different levels of SLA. Click on Help Topics > Add New Help Topic. Add the following topics: 

-Business Critical Outage

-Personal Computer Issues

-Equipment Request

-Password Reset

![image](https://user-images.githubusercontent.com/114452968/231040853-4162e024-fd32-4c8c-99a2-331c57c0ca67.png)
![image](https://user-images.githubusercontent.com/114452968/231040868-d707553d-1149-4ad3-a831-b069223a7c3b.png)
 
## Conclusion

This concludes our configuration and deployment phase. From a blank Helpdesk we have set up Admins, Support Agents, Roles, Departments, Teams, Users, a User Directory, SLA’s and Help Topics. In the next and final lab/tutorial we will walk through the lifecycle of a ticket submitted to our Helpdesk. 
