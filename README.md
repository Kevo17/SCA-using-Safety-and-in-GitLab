<h1>SCA using Safety and in GitLab</h1>


<h2>Description</h2>
In this lab, participants will learn how to perform Software Component Analysis (SCA) using Safety, an open-source security scanner, integrated within the GitLab CI/CD pipeline. Secure Code Analysis is a crucial step in the software development lifecycle to identify and address potential security vulnerabilities in code.
During the lab, participants will gain hands-on experience in setting up a GitLab CI/CD pipeline and configuring Safety as an automated SCA tool. They will explore the various features of Safety and understand how it can help detect common programming errors and security risks in their codebase.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Safety</b>
- <b>JSON</b>
- <b>GitLab</b>

<h2>Environments Used </h2>

- <b>Windows 11</b>
- <b>Linux</b> 

<h2>Program walk-through:</h2>

First, we need to download the source code of the project from our git repository: <br/>
```
git clone https://gitlab.practical-devsecops.training/pdso/django.nv webapp
```
<p align="center">
<img src="https://i.imgur.com/zvvF6rZ.png" height="80%" width="80%" alt="Disk Sanitization Step"/>
</p>

<br />
<br />

Lets cd into the application code, so we can scan the app: <br/>
```
cd webapp
``` 
<p align="center">
<img src="https://i.imgur.com/MbQK9JI.png" height="80%" width="80%" alt="Disk Sanitization Step"/>
</p>

<br />
<br />

Let’s install the safety tool on the system to scan the python dependencies: <br/>
```
pip3 install safety==2.3.5
``` 
<p align="center">
<img src="https://i.imgur.com/UwOujb1.png" height="80%" width="80%" alt="Disk Sanitization Step"/>
</p>

<br />
<br />

Lets explore what options safety provides us: <br/>
```
safety check --help
``` 
<p align="center">
<img src="https://i.imgur.com/UFsLyGh.png" height="80%" width="80%" alt="Disk Sanitization Step"/>
</p>

<br />
<br />

Lets check our source code with Safety: <br/>
```
safety check -r requirements.txt --json | tee safety-output.json
``` 
<p align="center">
<img src="https://i.imgur.com/UHgZ2k2.png" height="80%" width="80%" alt="Disk Sanitization Step"/>
</p>

<br />
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
