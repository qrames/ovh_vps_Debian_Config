# ovh_vps_Debian_Config

## Config your vps ovh Debian 9

### login :
* on your termminal :
>
yourname@machinename:~$ ssh root@51.51.192.251
root@51.51.192.251's password:
root@vps123456:~#

* vps123456 is your vps id */!\ you are root /!\* "root@vps123456:"
* make your user :
>
root@vps123456:~# adduser yourusername
Ajout de l'utilisateur « yourusername » ...
Ajout du nouveau groupe « yourusername » (1002) ...
Ajout du nouvel utilisateur « yourusername » (1002) avec le groupe « yourusername » ...
Création du répertoire personnel « /home/yourusername »...
Copie des fichiers depuis « /etc/skel »...
Entrez le nouveau mot de passe UNIX :

* create your password ...
##### login :
>
root@vps123456:~# su - yourusername
yourusername@vps123456:~$

* you can work on your systeme


### virtualenv Python :
#### pyhon2 config virtualenvwrapper:
*https://virtualenvwrapper.readthedocs.io/en/latest/install.html#python-version*

>
yourusername@vps123456:~$ apt install python-pip

<!-- pip install virtualenv ??? -->
>
yourusername@vps123456:~$ pip install virtualenvwrapper
yourusername@vps123456:~$ ls -a
.  ..  .bash_history  .bash_logout  .bashrc  .cache  .local  .nano .profile

in the *.bashrc* file you add lines for config your shell commende line on shell start
>
yourusername@vps123456:~$ nano .bashrc

>
...
 fi
fi
export WORKON_HOME=$HOME/.virtualenvs
export PROJECT_HOME=$HOME/Devel
export VIRTUALENVWRAPPER_VIRTUALENV=/home/yourusername/.local/bin/virtualenv
source ~/.local/bin/virtualenvwrapper.sh

*/home/yourusername/ or ~/*
* restart shell config :
>
yourusername@vps123456:~$ source nano .bashrc
