## Prerequisites - Setup the environment

Download vagrant and install it on your computer.

<img src="img/001-vagrant-download.png" width="60%"/>

Execute these command From the command line 
```console
$ mkdir datadog
$ cd datatadog
$ vagrant init ubuntu/xenial64
$ vagrant up
$ vagrant ssh
```

<img src="img/002-vagrant-ssh.png" width="60%"/>

## Datadog Agent installation

Browse to <a href="https://app.datadoghq.com/signup ">Datadog sign up page</a> an fill the form:

<img src="img/003-datadog-signup.png" width="60%"/>

Optionally, you can inform about the stack that you plan to use:

<img src="img/004-datadog-about-your-stack.png" width="60%"/>
 
Choose your platform (Ubuntu in our example) and copy your DataDog installation command:

<img src="img/005-datadog-installing-your-first-agent.png" width="60%"/>

Paste the installation command in the *vagrant ssh* terminal:

```console
$ DD_API_KEY=<YOU_API_KEY_HERE> bash -c "$(curl -L https://raw.githubusercontent.com/DataDog/datadog-agent/master/cmd/agent/install_script.sh)"
```

<img src="img/006-datadog-copy-installation-command.png" width="60%"/>

Wait until the agent installation is complete.

Now we can start working with DataDog:

<img src="img/008-datadog-dashboard.png" width="60%"/>

## Collecting Metrics:
* Add tags in the Agent config file and show us a screenshot of your host and its tags on the Host Map page in Datadog.

1. Browse to the folder **/etc/datadog-agent** and edit the file **datadog.yaml**
```console
$ cd /etc/datadog-agent
$ sudo nano datadog.yaml
```

2. Add this line:
```
tags: purpose:hiring, role:solutionsengineer, location:spain
```
<img src="img/009-datadog-tags.png" width="60%"/>

3. Restart your DataDog agent from the command line:
```console
$ sudo service datadog-agent restart
```

4. Click on **Events** option in you DataDog Admin panel. The new tags has been added:
<img src="img/010-datadog-events-new-tags.png" width="60%"/>
 
* Install a database on your machine (MongoDB, MySQL, or PostgreSQL) and then install the respective Datadog integration for that database.
* Create a custom Agent check that submits a metric named my_metric with a random value between 0 and 1000.
* Change your check's collection interval so that it only submits the metric once every 45 seconds.
* **Bonus Question** Can you change the collection interval without modifying the Python check file you created?





