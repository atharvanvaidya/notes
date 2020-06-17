# This page contains all the things that I learned while creating CTF Challenges

## Category : Forensics
* Always base64/32 encode the strings(flags) which are stored as it is, unless you want the solver to find it using strings.

* Windows XP stores the information (location, time of opening, etc of the file) about the files which are opened. This is visible in iehistory command of volatility. 

* The dump does not contain clipboard. 

* The VboxAdditions installed were visible in the dump file. So, don't install them

* The content opened in the notepad is directly visible by using strings. Also, notepad command is available in volatility

* 

## Category : 


## Links from JohnHammond's NahamCon 2020

* [Docker Compose](https://docs.docker.com/compose/)
* [Automatic CTF Deployment](https://blog.ctfd.io/automating-ctf-challenge-deployment-5f79022e310f)
* [Terraform](https://www.terraform.io/) - To automate the deployment and taking down process
* [CTFd-Docker-Challenges](https://github.com/offsecginger/CTFd-Docker-Challenges) - 

