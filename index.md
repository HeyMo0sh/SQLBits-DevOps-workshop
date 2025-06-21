---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
 
# SQL projects and source control integration for SQL in Fabric, Azure SQL, and SQL Server

## Summary

This workshop is a deep dive on database DevOps centered on the SQL database projects format, where you will learn practical techniques for managing database changes whether your workload is operational, analytical, or somewhere in between. Our exploration begins with the foundational CI/CD capabilities for SQL projects, where you can ensure no matter how a database is developed it is in source control and can be verified before deployments to one or more environments. The same shared SQL projects format applies to the whole Microsoft SQL family, so we'll examine the advantages and special capabilities to understand when implementing DevOps practices for Fabric SQL, Azure SQL, or SQL Server. We conclude our workshop with some special topics at the core of good data DevOps practices, including security management, static data management, and coordinating changes with other workloads.

## SQL Server Details

- Server:      sqlbits.database.windows.net
- Admin:       <contact Hamish Watson>
- Password:    <contact Hamish Watson>

## CodeSpace Install of SQLPACKAGE & .NET SDK

### .NET SDK

1. To install the .NET 8 SDK in a Codespace, follow these steps:

1. Open the terminal in your Codespace.
1. Download and install the .NET 8 SDK using the official Microsoft installation script:

``` bash
wget https://dot.net/v1/dotnet-install.sh -O dotnet-install.sh
chmod +x dotnet-install.sh
./dotnet-install.sh --channel 8.0
```

1. Add the installed .NET tools to your PATH:

``` bash
export DOTNET_ROOT=$HOME/.dotnet
export PATH=$PATH:$HOME/.dotnet
```

1. Verify the installation:

``` bash
dotnet --version
```

### SQLPACKAGE

1. To install sqlpackage in your Codespace (Linux), follow these steps in the terminal:

``` bash
wget https://aka.ms/sqlpackage-linux -O sqlpackage.zip
```

1. Extract the zip file:

```bash
unzip sqlpackage.zip -d sqlpackage
```

1. Move sqlpackage to a directory in your PATH (e.g., /usr/local/bin):

```bash
sudo mv sqlpackage /opt/sqlpackage
sudo chmod +x /opt/sqlpackage/sqlpackage
sudo ln -s /opt/sqlpackage/sqlpackage /usr/local/bin/sqlpackage
```

1. Verify the installation:

``` bash
sqlpackage -?
````

## Workshop labs

- [Lab 0: Setup](LAB0/)
- [Lab 1: Participants configure a simple CI/CD pipelines for a sample SQL project](LAB1/)
- [Lab 2: Participants deploy SQL projects to different platforms](LAB2/)
- [Lab 3: Participants implement advanced DevOps practices in their SQL projects](LAB3/)
- [Lab 4: Troubleshooting and Optimizing DevOps Workflows](LAB4/)

### [Lab 1](LAB1/): Participants configure a simple CI/CD pipelines for a sample SQL project

- 1.1: Create a project from an existing database
- 1.2: Create a pipeline to publish the project to the database
- 1.3: Create a pipeline to build the project and run code analysis
- 1.4: Deploy our changes to the database

### [Lab 2](LAB2/): Participants deploy SQL projects to different platforms

- 2.0: Update your local repository from GitHub
- 2.1: Create a pipeline for SQL Server 2022
- 2.2: Create a SQL database in Fabric and use source control integration

### [Lab 3](LAB3/): Participants implement advanced DevOps practices in their SQL projects

- 3.1: Static data management through a post-deployment script
- 3.2: Deploy script and environment approvals
- 3.3: Deploy report and summarizing dangers

### [Lab 4](LAB4/): Troubleshooting and Optimizing DevOps Workflows

- 4.1: Creating a rollback point when the deployment is successful
- 4.2: Incorporating data cleaning pre-deployment scripts
- 4.3: Source control for a rogue database

## Workshop contents

This site provides a walk-through of the workshop labs with checkpoints that can be expanded to check your work. The contents of this site are available at [https://github.com/HeyMo0sh/SQLBits-DevOps-workshop](https://github.com/HeyMo0sh/SQLBits-DevOps-workshop), including the full expected results of each lab. This project is licensed under the MIT License such that it can be used in whole or part to help others improve their database DevOps implementations - see the [LICENSE](LICENSE.md) file for details.

If you have feedback about the workshop, open an issue to share your thoughts, suggestions, or any issues you encounter. Pull requests are also welcome if you want to contribute to workshop content. Check out the [CONTRIBUTING](/contributing/) page for more information on how to contribute.

## About the initial authors

### Drew Skwiers-Koballa

[Drew Skwiers-Koballa](https://www.linkedin.com/in/drew-skwiers-koballa/) is a Principal Program Manager at Microsoft, focusing on building tools that make databases more accessible and powerful for developers. Before joining Microsoft in 2020, he spent nearly a decade as a developer, database administrator, and team lead. Drew immensely enjoyed being a technical reviewer for the book "Practical Azure SQL Database for Modern Developers." As a relentless learner and occasional developer, his work spreads across several blogs, videos, and samples linked from https://github.com/dzsquared. He has an MS in computer science from Georgia Tech and an MS in chemistry from the University of Minnesota.

**Drew is incredibly grateful to Heidi and Hamish for their partnership on this workshop - from the content to the initial delivery at Fabric Conference 2025, their expertise and enthusiasm for DevOps practices with databases has been invaluable.**

### Hamish Watson

[Hamish Watson](https://www.linkedin.com/in/hamishwatson8/) is a Microsoft Data Platform MVP with a passion for efficient database & application deployments using DevOps methodologies.

He has formed his own company – Morph iT Limited – based in Christchurch, New Zealand and provides consultancy services for many clients in the US, Canada, UK, Australia and NZ.

He also has created a small startup called [MakeStuffGo](https://www.makestuffgo.com) this company is dedicated to bringing AI services to both Cloud and DevOps Engineering practices.  

Want to see how your company stacks up against DevOps, FinOps and Cloud industry standards?

Take the [FREE DevOps & Finops Assessment Guide](https://assessment.makestuffgo.com)

He has 25+ years IT experience in managing and deploying large scale applications using various technologies. He has been managing SQL Server since SQL Server 2000 and pragmatic approaches to delivering business value is his career passion.

Educating and helping others learn is a driver for Hamish and he is a User Group Leader, International speaker and a repeat guest lecturer at universities.

### Heidi Hasting

[Heidi Hasting](https://www.linkedin.com/in/heidi-hasting-a068694/) is a Business Intelligence professional and former software developer with over seven years experience in Microsoft products. She is an ALM/DLM enthusiast and Azure DevOps fan and co-founder and organiser of the Adelaide Power BI User Group. Heidi is a regular attendee at tech events including Azure Bootcamps, DevOps days, SQLSaturdays, Difinity and PASS Summit.

