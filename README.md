# Setting Up Sonar Server for VSTS 2017.

### Minimum Deployment

-   All TFS Services, SQL Server and SonarQube, including Sonar Runner and Build Controller) hosted on a single computer.
-   Suitable for research, dogfooding and demonstration of entire end-to-end workflow on one machine.

	**>> NOTE >>** In this guide, we will demonstrate the installation and configurations using an Azure VM server 2012 r2 and sql 2014 express. 

### Medium Deployment

- TFS Services and SQL Server are hosted on a single computer and SonarQube (all components) on a separate machine.
- Suitable for evaluation in production or near-production environments.


1. **Download**
	- Download **SonarQube 6.3.1** from the SonarQube [downloads](https://www.sonarqube.org/downloads/).

		
	- As mentioned in the Prerequisites section, a Java virtual machine (JVM) is required.
	- If the installed JVM meets the version requirements listed, you can skip this section. Otherwise, follow the steps below to install Java.
	- Download [Java SE Runtime Environment](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) and make sure you select the one corresponding to your current operation system.
	
> > ![](images/sonar1.PNG)
		
**>> NOTE >>** SonarQube does not require the full Java JDK (Java SE Development Kit) to run- you only need the JRE (Java SE Runtime Environment).


2. **Install Java JRE**
	- Install **Java SE Runtime Environment** on the destination server.
	
> > ![](images/sonar2.png)

3. **Configure sql server**

Before you get to the task of creating a new database for SonarQube, you need to complete a few preparations.

1. **Launch SSMS**
	- Launch **SQL Server Management Studio** (SSMS).
	- Connect to the SQL Server instance on which you plan to create the database.

> -Create a user with SQL Server authentication, called sonar with a password.

> -Security > right click on Logins > New Login.

> > ![](images/sonar3.PNG)

> > ![](images/sonar4.PNG)

> Then you should open Sql Server Configuration Manager, and you must enable the TCP Procol.

> > ![](images/sonar5.PNG)

> Open Properties for TCP/IP protocol. 

> Disable dynamic ports and specify 1433 as TCP Port.

> > ![](images/sonar6.PNG)





How to create a SonarQube server on Azure with Template

https://github.com/Azure/azure-quickstart-templates/tree/master/sonarqube-azuresql

Ones done address is:  

#####http://[sq_PublicIP_DnsPrefix].[AzureRegion].cloudapp.azure.com:9000
Ex: http://my-sonarqube.westeurope.cloudapp.azure.com:9000 Ex: Secure https://my-sonarqube.westeurope.cloudapp.azure.com
