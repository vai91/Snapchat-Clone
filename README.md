<p align="center">
<a href="https://www.gitignore.io">
<img src="https://cdn.rawgit.com/joeblau/gitignore.io/master/Public/img/gitignoreio.svg" />
</a>
<br>
<strong>Create useful .gitignore files for your project</strong>
</p>
<p align="center">
<a href="https://swift.org"><img src="https://img.shields.io/badge/Swift-3.1-orange.svg"/></a>
<a href="https://travis-ci.org/joeblau/gitignore.io"><img src="https://img.shields.io/travis/joeblau/gitignore.io.svg" alt="Travis"></a>
<a href="https://codecov.io/gh/joeblau/gitignore.io"><img src="https://img.shields.io/codecov/c/github/joeblau/gitignore.io.svg" alt="Codecov"></a>
<a href="https://codebeat.co/projects/github-com-joeblau-gitignore-io"><img src="https://codebeat.co/badges/466223cd-3a95-40a9-80e4-09690915ae93" alt="codebeat badge"></a>
<img src="https://img.shields.io/badge/Platforms-Linux%20%7C%20macOS%20%7C%20Windows-blue.svg"alt="Platforms">
<a href="https://github.com/joeblau/gitignore.io/blob/master/LICENSE.md"><img src="https://img.shields.io/github/license/joeblau/gitignore.io.svg" alt="license"></a>
</p>
#  Instructions 
1) Download the ParseStarterProject.zip, then create an account from Amazon Web Services
2)Create an instance of EC2 with new key value pair, download the .pem file(key)
3)Add Parse Server from AWS Marketplace(use free version)
4)Connect to your instance using an SSH Client(install PuTTY for Windows, for mac, don't need to install anything, change the permissions of the .pem file to chmod 400
ssh -i "/Location/of/the/document/snapchatkeypair.pem" ubuntu@yourUniquePublicDns.compute.amazonaws.com)
5)We need to change the settings(cd apps/parse/htdocs)
6)Open server.js file in it (nano server.js)
7)In order for your app to connect to the server, you need to provide keys in AppDelegate.swift file.
Copy these from server.js file -> 'appId', 'masterKey','serverURL' 
and paste them into 'applicationId', 'clientKey', 'server' on AppDelegate.swift
8)Go to the URL/apps, which will take you to Parse Dashboard. There you can see everything you saved for your users, usernames, pictures etc.
To retrieve your password, click the bottom-right corner, and follow the instructions.
Actions->Instance settings->Instance log(get the password from there on EC2 Dashboard)
9)Login to the Parse Server Dashboard using the credentials(username->user)
10)Run the project now. On ViewController.swift file there's a test object being created, we now check if we can see it through the dashboard. 
If on the dashboard you see TestObject2, you're good! 
So far we accomplished a huge deal of stuff! 
We've created an EC2 instance on our web server from amazon, installed parse on it, we connected to it using our app, and saved some data on it! 

