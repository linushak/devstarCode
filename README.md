
# Become the Dev Star #

## Introduction ##

<img src="images/spaceship.png">

In this adventure you will pledge allegiance to one of the rebel squads, everyone sharing the same goal  – becoming the Dev Star.

Choose your space fighter platform of choice (Node.js, Java or PHP) and develop and deploy cloud native microservices that will help defeat the Alien War Ship.

To complete the different missions, you will build, manage and deploy cloud native microservices.

+ You will use GitHub to manage the source control. You will use Wercker for continuous integration and continuous deployment of your microservices, in a quick and agile way.
+ You will explore and perform actions related to scaling and operating your microservices.
+ You will use your creativity to develop features to your microservices that will help your squad win!

## Introduction ##

The Alien War Ship needs to be defeated. You, your squad and your space microservice fighters are the last hope for planet Earth!

The adventure is intense and a set of missions must be accomplished in order to achieve the desired victory! 

<img align="left" src="images/devstar_spy.png" width = "60px">

Fortunately, one of our companions is a spy, Tom Kurious, and he have managed to sneak into the Alien War Ship. During our missions, he will report valueable information that might help us to bring down the Alien War Ship!

## How to play ##

#### Objective ####

By developing space fighters (microservices) in either Java, Node.js or PHP, you will complete missions in order to defeat the Alien War Ship. The missions will be explained in the instructions below, but you can't complete some of the missions without valuable information from the spy.

## Scoring ##

Your squad will get points as you complete missions. When you have completed all the missions - you will be placed on the Hall Of Fame list and can title yourself a Dev Star! The quicker you complete the missions, the higher you will place yourself on the Hall of Fame list.

## Let's go! ##

 It is now time to select your weapon of choice.

+ Weapon selection strategy is completely up to your preference.
+ Each git repository includes the basic code that is needed in order to run and deploy your microservice to the battle action!

| [![Node](images/nodejs.png)](https://github.com/thebeebs/xwingnodeclient) | [![Java](images/javase.png)](https://github.com/thebeebs/xwingjavaclient) | [![PHP](images/php.png)](https://github.com/thebeebs/xwingphpclient) |
|:---:|:---:|:---:|

| Weapon        | Git Repo to Fork  |
| ------------- | -----|
| Node.js       |https://github.com/oracledevstar/nodecode|
| Java SE     |   https://github.com/oracledevstar/javacode |
|PHP | https://github.com/oracledevstar/phpcode |

1. Click on your preferred weapon's Git repository above and fork into your own repository. 
<img src="images/github_fork.png">

## Mission: Deploy your first fighter! ##

### Mission Description ###

In order to take up the battle against the Alien War Ship, your need to deploy your space fighter (microservice) to the cloud.

### Mission Awards ###

- Number of points for this mission: **100**

### Mission Instructions ###

To deploy your fighter, you will use Continuous Integration and Deployment.
+ First you will connect your cloned GitHub repostiory to a Continuous Integration and Deployment pipeline using Wercker.
+ You will then perform a change on your code.
+ Werker will then automatically build, package and deploy your application to Application Container Cloud. 

**Setting up the Continuous Integration and Deployment pipeline

1. Open a new window/tab on [https://app.wercker.com](https://app.wercker.com) and use the "Sign in with GitHub" button.

<img src="images/wercker_signin.png">

2. Press Authorize Wercker

3. Fill in a desired username and email address and press Finish Up.
<img src="images/wercker_setup.png">

4. On the landing page, press **Create your first application**. Alternatively, select **Pipelines** and click **Create an application** to create a new pipeline. 

<img src="images/wercker_welcome.png">

5. Select the application owner. Use the default user and don't select an organization in case you already have one. Press **Next**.

6. Now select the repository you just forked and click **Next**.

7. For the Configure Access dialog, keep the default and press **Next**.

8. Finally, press **Create** to create your application.

It is now time to configure the deployment pipeline. For Wercker to know how it should deploy your application to the Oracle Application Container Cloud, it will need a couple of environment properties. 

9. Go to the Enviroment tab.

<img src="images/wercker_envTab.png">

10. **Now is the time to select your squad!** Have a look at the squad credentials document. Note that the username, password, identity domain and identifier are unique for a squad. **Make sure your select the credentials for the squad you want to belong to!**
Fill in the environment variables based on your squad's credentials like below.

<img src="images/wercker_envProps.png">

### Ready to Deploy

1. Let's first make a change to github to check the build and deploy is now working, when you checkin a difference in the repository is identified and the build job is properly triggered in Wercker.
So, depending on the language you chose, have your code opened and make the suggested change:

 **Node.JS**: Open the file *xwingnodeclient/app.js* and on the first line insert a comment line with some text.
```                       
eg: // My microservice!
```
 **Java**: Open the file *src/main/java/com/example/rest/App.java* and on the first line insert a comment line.
```
 eg: // My microservice!
```
 **PHP**: Open the file *index.php* and edit the line on row 2 (below "<php") and insert a comment line.
```
eg: // My microservice!
```
2. Save the file

3. Check the file into Git if you are working locally.
```
git add .

git commit -m "My first commit"

git push
```
Or you could edit directly in GitHub.

4. Monitor the Dev Star dashboard to await your fighter being deployed! If you can't see the Dashboard well on the projector/screen, just open the following url http://129.144.148.225. Your space fighter should appear in the dashboard and complete it's first strike to the Alien War Ship!

## Mission: Scale your first fighter! ##

### Mission Description ###

Your squad has now deployed one or several individual microservices (fighters). Our next mission will be add to another fighter to the squad by scaling up the number of instances for your fighter.

### Mission Awards ###

- Number of points for this mission: **100**

### Mission Instructions ###

1. Sign in to Application Container Cloud using the URL and credentials for your squad.

The URL is: https://apaas.europe.oraclecloud.com/apaas/faces/aPaaSRunner.jspx

2. Click your deployed application (yours is identified by your GitHub username):

3. Click your deployed application. If your microservice is deployed, you can view the logs. [Click here](../logs.md) for instructions on how to view the logs. **Before you continue to the next step, make sure that you are able to retrieve and read the logs from your running application!**

4. You should now understand how to view the logs of your deployed application, if not, check the previous step before you continue. Increment the number of instances to 2. Please note that adding more than 1 instances do not give you any more points or advantages.

## Mission: Take down the shield! ##

### Mission Description ###

Your squad is ready and it should now have one or more microservices with at least one of them having 2 instances.
<img align="right" src="images/spaceship_shield.png" width = "400px">
The Alien War Ship is protected by it's powerful shield. As long as we can't break through the shield, we will have a hard time hitting the core reactors of the Alien War Ship.

### Mission Awards ###

- Number of points for this mission: **300**

### Mission Instructions ###

1. To start firing at the shield, we first need to have the Alien War Ship exposing it's coordinates. In the Dashboard, click on the Spy to see if he has anything to reveal.Q

2. We now need to fire at the coordinates of the shield! You will do this by changing the code in your microservice and deploy the new version. 

- For Java, the file is located at src/main/java/com/example/rest/App.java (in the folder where you locally cloned the code)
- For Node.js, the file is located at xwingnodeclient/app.js (in the folder where you locally cloned the code)
- For PHP, the file is located at index.php (in the folder where you locally cloned the code)

The base URL of the shield is ```http://129.144.148.225:3000/shield/x-coordinate_goes_here/y-coordinate_goes_here/Your_squad_color_goes_here(e.g yellow)/Your_microservice_name_goes_here(e.g YellowJava2Fighter)```. **The shield will get hit by HTTP GET Request bullets!**

**Hint: Make sure that your code/function is actually being called **

You need to look through your App.java, app.js or index.php file depending on your language and find out what changes you will need to make to invoke the shield's URL!

3. Deploy a new version of your microservice by pushing the edited code to the Git repository in the same way as for your first deployment. 

4. When your updated microservice is live, it will hopefully hit the Alien War Ship's shield!

5. If you feel that your microservice is not behaving correctly or might not have been deployed correctly, have a look at the logs as described [here](../logs.md).

## Mission: Shoot down the Mini Fighters ##

### Mission Description ###

<img align="right" src="images/fighters.png" width = "300px">
The Alien War Ship has sent out 10 Mini Fighters to attack your fighters! You need to take them down as soon as possible. The mission is completed when a squad has shot down all the Mini Fighters.

### Mission Awards ###

- Number of points for this mission: **500**

### Mission Instructions ###

1. You should now have received information from the spy that will give you the y-coordinates of the Mini Fighters. The example below would shoot down ***one*** of the Mini Fighters. ***The x-coordinate is always locked at coordinate 45***.

```http://129.144.148.225:3000/fighters/45/y-coordinate_goes_here/Your_squad_color_goes_here(e.g yellow)/Your_microservice_name_goes_here(e.g YellowJava2Fighter)```. **The Mini Fighters will get hit by HTTP GET Request bullets!**

**Hint: Notice the changed endpoint 'fighters'**

3. Deploy a new version of your microservice by pushing the edited code to the Git repository in the same way as for your first deployment.

3. When your updated microservice is live, it will hopefully hit the Mini Fighters sent out by the Alien War Ship!

4. If you feel that your microservice is not behaving correctly or might not have been deployed correctly, have a look at the logs as described [here](../logs.md).

## Mission: Destroy the Reactor Core! ##

### Mission Description ###

<img align="right" src="images/spaceship_core.png" width = "400px">
The spy should now have exposed the secrets of the database where the Alien War Ship stores the coordinates to it's Reactor Core! When our spy returns with the information, find out the coordinates and attack it with your fighter!

### Mission Awards ###

- Number of points for this mission: **500**

### Mission Instructions ###
1. You should now have received information from the spy about the credentials to the Alien War Ship's MySQL database where the coordinates for the Core Reactor is kept. Develop a MySQL query that queries the **SecretTable** to retrieve information about the Reactor Core coordinates! The Host IP address of the database is  **129.144.148.225**

2. When you have the coordinates, hit the Reactor Core at the following URL:
```http://129.144.148.225:3000/reactorCore/x-coordinate_goes_here/y-coordinate_goes_here/Your_squad_color_goes_here(e.g yellow)/Your_microservice_name_goes_here(e.g YellowJava2Fighter)```.
**The Reactor Core will get hit by HTTP GET Request bullets!**

**Hint: Notice the changed endpoint 'reactorCore'**

3. Deploy a new version of your microservice by pushing the edited code to the Git repository in the same way as for your first deployment.

4. When your updated microservice is live, it will hopefully hit the Alien War Ship's Reactor Core!

5. If you feel that your microservice is not behaving correctly or might not have been deployed correctly, have a look at the logs as described [here](../logs.md). 

### You are finished ###

Congratulations! You are finished and you have shut down the Alien War Ship. You can now title yourself a Dev Star. Check out the Hall of Fame on the dashboard for your final ranking!

### Next Step ###

Take a Fee $300 trail out today http://thebeebs.uk/codeadventures (speak to Thrasos if you are having trouble) and create your own ACCS (Application Container Cloud Cluster). Once you have created it and deployed an application to it let me know at martin.beeby@oracle.com and I will send you some Oracle goodies as a thank you.








