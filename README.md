# YOMoni
by Jens De Vreese, Frederik Van Brussel

## Dependencies

In order to set up this environment, you need:

* [Git](https://git-scm.com/downloads) (including Git Bash)
* [VirtualBox, including the "Extension pack"](https://www.virtualbox.org/wiki/Downloads/)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [Ansible](http://docs.ansible.com/intro_installation.html) (on [supported platforms](http://docs.ansible.com/intro_installation.html#control-machine-requirements))

## Getting started

Open a Bash shell (Git Bash on Windows), go to a suitable directory to store this project and issue the following commands:

```ShellSession
$ git clone --config core.autocrlf=false https://github.com/lilswif/yomoni.git
$ cd yomoni
```

in the file ```ansible/host_vars/yomoni.yml``` you can use the ansible variable ```siege_targets```
to add sites wich siege will attack.

eg.
``` 
siege_targets:
  - 192.168.56.77/wordpress 
  - www.atestwebsite.co
```

> note: This can always be altered in the guest by the command ```sudo vi /usr/local/etc/urls.txt```

now its time to launch our virtual machine through the commandline:
```Shellsession
$vagrant up
```
Next, time to ssh in our machine with ```vagrant ssh```.

## Configure Siege strategy and attack

!!! Always run the following commands run from the ```/home/vagrant/yomoni``` folder !!!

To configure the siege strategy, launch following command:
```
sudo vi config.cfg
```

Following variables can be changed:
| Variable  | value(s) | required |  explanation |
| :---     	|    ---:  |     ---: |    ---: |
| RANGE     |  TRUE / FALSE|yes|  if true, Siege will test all numbers of users between a interval, including start en stop value |

