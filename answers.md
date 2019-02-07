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
 
Choose your platform and copy you DataDog API KEY:

<img src="img/005-datadog-installing-your-first-agent.png" width="60%"/>


