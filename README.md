# Ansible PHP Website
## Description
This is a simple ansible project that uses Vagrant to provision an Ubuntu Virtual Machine and Ansible to setup FPM, Nginx to run a trivial application.

## Setup & Usage
To run this you will need to make sure your system has `vagrant` as well as `ansible` installed.

```
$ vagrant up
$ ansible-playbook ansible/site.yaml -i ansible/hosts
```

Make sure to add the domain `hello.world` redirecting to `10.0.0.10` in your `/etc/hosts` file of your host.
You may achieve this with the following command:

```
$ echo -e '10.0.0.10\thello.world' |sudo tee -a /etc/hosts
```

Fire up your web browser and browse to the address `http://hello.world`. You should be able to access the test website.
