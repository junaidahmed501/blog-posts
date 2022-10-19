# Setting up your system (Ubuntu 18.04) to run different versions of Python & Django

I started this guide as a cheat sheet for myself for the times when I needed to created **Django** project or when I needed to run multiple **Python** versions. This is an all-rounder guide towards having multiple Python versions even if we don’t need Django.

Ubuntu 18.04 comes pre installed with python version 3 & 2. To check those two, write ***python*** or ***python3*** in your terminal.

junaid@johnny:~$ python

Python 2.7.17 (default, Nov 7 2019, 10:07:09)   
\[GCC 7.4.0\] on linux2  
Type “help”, “copyright”, “credits” or “license” for more information.  
\>>>

junaid@frt-eh:~$ python3

Python 3.6.9 (default, Nov  7 2019, 10:44:02)   
\[GCC 8.3.0\] on linux  
Type "help", "copyright", "credits" or "license" for more information.  
\>>>

How to install softwares from tar/tgz files (.tar.gz or simply .tar)

[**What is a tar.gz File, and How Do I Open It?**  
*A tar file, often called a tarball, is a collection of files wrapped up in one single file for easy storage. Rather…*www.howtogeek.com](https://www.howtogeek.com/362203/what-is-a-tar.gz-file-and-how-do-i-open-it/ "https://www.howtogeek.com/362203/what-is-a-tar.gz-file-and-how-do-i-open-it/")[](https://www.howtogeek.com/362203/what-is-a-tar.gz-file-and-how-do-i-open-it/)

[https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-ubuntu-18-04-quickstart](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-ubuntu-18-04-quickstart)

[https://hackersandslackers.com/multiple-versions-python-ubuntu/](https://hackersandslackers.com/multiple-versions-python-ubuntu/)

[**How to Upgrade to Python 3.7 on Ubuntu 18.04/18.10**  
*Disclaimer Edited: 2020-03-10 15:54:45 UTC Instead of using below method please consider adding a new/multi python…*tech.serhatteker.com](https://tech.serhatteker.com/post/2019-09/upgrade-python37-on-ubuntu18/ "https://tech.serhatteker.com/post/2019-09/upgrade-python37-on-ubuntu18/")[](https://tech.serhatteker.com/post/2019-09/upgrade-python37-on-ubuntu18/)

[**How to Upgrade to Python 3.7 on Ubuntu 18.04/18.10**  
*Disclaimer Edited: 2020-03-10 15:54:45 UTC Instead of using below method please consider adding a new/multi python…*tech.serhatteker.com](https://tech.serhatteker.com/post/2019-09/upgrade-python37-on-ubuntu18/ "https://tech.serhatteker.com/post/2019-09/upgrade-python37-on-ubuntu18/")[](https://tech.serhatteker.com/post/2019-09/upgrade-python37-on-ubuntu18/)

**Virtual Environment & pip**

[https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/)

[**How to Install Pip on Ubuntu 18.04**  
*Pip is a package management system that simplifies installation and management of software packages written in Python…*linuxize.com](https://linuxize.com/post/how-to-install-pip-on-ubuntu-18.04/ "https://linuxize.com/post/how-to-install-pip-on-ubuntu-18.04/")[](https://linuxize.com/post/how-to-install-pip-on-ubuntu-18.04/)

### ***How to create Django project***

***Note:*** commands containing 3 are recommend because they use python 3 & all.

[**Starting a Django Project - Real Python**  
*Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design. In this…*realpython.com](https://realpython.com/django-setup/ "https://realpython.com/django-setup/")[](https://realpython.com/django-setup/)

1.  check (python -V or python3 -V) & install your python version (if necessary)
2.  install pip **and/or** pip3  
    sudo apt -y install python-pip  
    sudo apt -y install python3-pip
3.  instal virtualenv  
    `sudo pip install virtualenv  
    sudo pip3 install virtualenv`   
    ***or*** venv  
    `***sudo apt install python3-venv***`
4.  create virtual env to for you app (create a directory & execute in that folder)  
    `virtualenv my-project-env  
    virtualenv -p /usr/bin/python2.7 .venv  
    **using venv  
    **python3 -m venv my-project-env`
5.  activate virtual env  
    `source my-project-env/bin/activate`
6.  create django project (the actual application which will contain our views & controllers & all)  
     — — rest of the steps coming soon — —

helpful links:

[**How to Create Python Virtual Environments on Ubuntu 18.04**  
*Python virtual environment is a self-contained directory tree that includes a Python installation and number of…*linuxize.com](https://linuxize.com/post/how-to-create-python-virtual-environments-on-ubuntu-18-04/ "https://linuxize.com/post/how-to-create-python-virtual-environments-on-ubuntu-18-04/")[](https://linuxize.com/post/how-to-create-python-virtual-environments-on-ubuntu-18-04/)

[**How to install virtualenv on Ubuntu 18.04**  
*We may face issues when our Linux distribution only offers certain versions of Python and its packages, when we…*dev.to](https://dev.to/serhatteker/how-to-install-virtualenv-on-ubuntu-18-04-2jdi "https://dev.to/serhatteker/how-to-install-virtualenv-on-ubuntu-18-04-2jdi")[](https://dev.to/serhatteker/how-to-install-virtualenv-on-ubuntu-18-04-2jdi)