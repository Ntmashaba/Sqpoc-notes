SQL Code Analysis Project
This project enables you to perform code analysis on SQL scripts using SonarQube and SonarScanner for MSBuild. The purpose is to enhance code quality by analyzing your SQL source code, identifying issues, and providing insights to address them.

SQL Source Code and Project File
The project contains a SQL project file Database1.sqlproj with a standard header. The SQL script files to be included in the build should be listed in the project file. In this case, TestScript.sql is listed in the Database1.sqlproj file.

Prerequisites
SSDT (SQL Server Data Tools) installed on the host machine
Docker installed to run SonarQube
Download the SonarScanner for MSBuild and extract it to the sonar-scanner folder
Project Structure
The project should have the following structure:

A sonar-scanner folder containing the contents of SonarScanner.MSBuild
A src folder containing the TestScript.sql file and the Database1.sqlproj file
Setting up SonarQube
Pull the SonarQube Developer image: docker pull sonarqube:developer
Run the SonarQube Developer image in Docker on port 9000: docker run -d --name sonarqube -p 9000:9000 sonarqube:developer
Open your browser and navigate to http://localhost:9000. Log in using the default credentials (username: admin, password: admin).
Update your credentials as prompted upon first login.
Enter your SonarQube Developer Edition license key.
Configure the server for PL/SQL and T-SQL:
Go to the Administration tab > Configuration > Languages.
From the dropdown, select PL/SQL. Remove the .sql file suffix and save.
Now, select the T-SQL language. Change the file suffix to .sql from .tsql. Save.
Running the project
Open a command prompt in the project folder and execute the following commands:
Begin the SonarScanner analysis: dotnet ./sonar-scanner/SonarScanner.MSBuild.dll begin /k:"MyProjectName" /d:sonar.host.url="http://localhost:9000" /d:sonar.login=SONAR_TOKEN
Build the SQL project: msbuild src\Database1.sqlproj /t:Rebuild /p:Configuration=Release
End the SonarScanner analysis: dotnet ./sonar-scanner/SonarScanner.MSBuild.dll end /d:sonar.login=SONAR_TOKEN
Wait for the analysis to complete and view the results on the SonarQube dashboard at http://localhost:9000.
