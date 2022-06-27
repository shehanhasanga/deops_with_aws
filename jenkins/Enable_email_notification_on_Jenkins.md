# Enable email notification on Jenkins


## Integration Steps
Log into the Jenkins to install mailer plugin

1. Install "mailer" plug-in   
- `Manage Jenkins` -> `Manage Plugins` -> `available` -> `mailer`

2. Configure Mailer   
- `Manage Jenkins` -> `Configure System`
    - E-mail Notification:
    - SMTP server : `smtp.gmail.com`
  - Advanced: 
	- [x] `Use SMTP Authentication` 
	- User Name : `valaxytech@gmail.com`
	- Passwrod : `<password>`   
  - [x] `Use SSL`
	- SMTP Port: `465`
	- Charset : `UTF-8 (Auto filled)`

  
1. Create a new job 
  - Job Name : `test-email-job`
  - Source code management 
     - Git URL : [get URL here](https://github.com/yankils/hello-world.git)
 - Build Environment 
     - Maven3-Artifactory Integration : `<provide Artifactory server and repository details
>`
 - Build --> Invoke Artifactory Maven3  
       - Goals: ` clean install`

# Still working 
