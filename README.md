# Engineering89 Jenkins Provision Task
This repo is all you need to get started running a Jenkins instance on your own Vagrant machine!

## How to run
1. Make sure [Vagrant](https://www.vagrantup.com/) and [Virtual Box](https://www.virtualbox.org/) are installed as these are required to run the file
2. Clone this repository
3. Run the `Vagrant` file!
4. Take a quick break, it can take a few minutes to install
5. Navigate to `192.168.10.100:8080`
6. Complete the [setup process](https://www.jenkins.io/doc/book/installing/linux/#setup-wizard)

If you need the admin password to complete setup, simply run this command:
```console
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
In your vagrant ssh terminal to get the password


## AWS
If you wish to get automatic setup in AWS, the process is quite simple.

1. Set up your AWS instance as you normally would until you get to step 3
2. When you reach step 3 you will need to locate the "User data" field
3. Select "use file" and upload the `provision_jenkins.sh` file
4. Continue setup as usual
5. Wait. It may take a while to install
6. Navigate to your AWS instance and append `:8080` to the IP address
7. Complete the [setup process](https://www.jenkins.io/doc/book/installing/linux/#setup-wizard)