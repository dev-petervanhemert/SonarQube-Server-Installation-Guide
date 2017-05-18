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

		![](_img/SonarQube.Download.png)
	- As mentioned in the Prerequisites section, a Java virtual machine (JVM) is required.
	- If the installed JVM meets the version requirements listed, you can skip this section. Otherwise, follow the steps below to install Java.
	- Download [Java SE Runtime Environment](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) and make sure you select the one corresponding to your current operation system.

		![](_img/JavaSeRuntimeEnvironment.png)
		
		**>> NOTE >>** SonarQube does not require the full Java JDK (Java SE Development Kit) to run- you only need the JRE (Java SE Runtime Environment).


















How to create a SonarQube server on Azure with Template

https://github.com/Azure/azure-quickstart-templates/tree/master/sonarqube-azuresql

Ones done address is:  

#####http://[sq_PublicIP_DnsPrefix].[AzureRegion].cloudapp.azure.com:9000
Ex: http://my-sonarqube.westeurope.cloudapp.azure.com:9000 Ex: Secure https://my-sonarqube.westeurope.cloudapp.azure.com
