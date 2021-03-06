Simple Flask App
================

Aplikacja Dydaktyczna wyświetlająca imię i wiadomość w różnych formatach dla zajęć
o Continuous Integration, Continuous Delivery i Continuous Deployment.

- Rozpocząnając pracę z projektem (wykorzystując virtualenv). Hermetyczne środowisko dla pojedyńczej aplikacji w python-ie:

  ::

    # centos, add to ~/.bashrc
    $ source /usr/bin/virtualenvwrapper.sh

    # ubuntu, add to ~/.bashrc
    $ source /usr/local/bin/virtualenvwrapper.sh

    $ mkvirtualenv wsb-simple-flask-app
    $ pip install -r requirements.txt
    $ pip install -r test_requirements.txt

  Sprawdź: `documentację virtualenvwrappera <https://virtualenvwrapper.readthedocs.io/en/latest/command_ref.html>`_.

- Uruchamianie applikacji:

  ::

    # jako zwykły program
    $ python main.py

    # albo:
    $ PYTHONPATH=. FLASK_APP=hello_world flask run

- Uruchamianie testów (see: http://doc.pytest.org/en/latest/capture.html):

  ::

    $ PYTHONPATH=. py.test
    $ PYTHONPATH=. py.test  --verbose -s

- Kontynuując pracę z projektem, aktywowanie hermetycznego środowiska dla aplikacji py:

  ::

    $ source /usr/local/bin/virtualenvwrapper.sh # nie trzeba, jeśli już w .bashrc
    $ workon wsb-simple-flask-app

    ...

    # deaktywacja virtualenv
    $ deactivate

- Integracja z TravisCI:

  ::

    ...


Pomocnicze
==========

Ubuntu
------

- Instalacja python virtualenv i virtualenvwrapper:

  ::

    $ sudo su
    $ pip install virtualenv
    $ pip install virtualenvwrapper

- Instalacja dockera: `dockerce howto <https://docs.docker.com/install/linux/docker-ce/ubuntu/>`_

Centos
------

- Instalacja python virtualenv i virtualenvwrapper:

  ::

    $ yum install -y python-pip
    $ pip install -U pip
    $ pip install virtualenv
    $ pip install virtualenvwrapper

- Instalacja docker-a:

  ::

    $ yum remove docker \
        docker-common \
        container-selinux \
        docker-selinux \
        docker-engine

    $ yum install -y yum-utils

    $ yum-config-manager \
      --add-repo \
      https://download.docker.com/linux/centos/docker-ce.repo

    $ yum makecache fast
    $ yum install -y docker-ce
    $ systemctl start docker

Materiały
=========

- https://virtualenvwrapper.readthedocs.io/en/latest/
test


Aby w domu sobie to odpalić to:
git clone path_to_repository:
$ vim ~/.gitconfig

$ git config --global user.name "USERNAME"
$ git config --global user.email "USERNAME@users.noreply.github.com"

# VIM
$ sudo apt-get update
$ sudo apt-get install vim

#
$ sudo pip install virtualenv
$ sudo pip install virtualenvwrapper

#
$ cd he...
$ source /usr/local/bin/virtualenvwrapper.sh
$ mkvirtualenv wsb-simple-flask-app

$ make deps
$ make test
$ make run


# tak żeby zobaczyć w jakim
# stanie zostawiliśmy nasz projekt
$ make lint

monitoring mozna zobaczyc na statuscake.com

Badge z travis CI

|build passing|

.. |build passing| image:: https://travis-ci.org/njaworek/se_hello_printer_app.svg
   :target: https://travis-ci.org/njaworek/se_hello_printer_app

Badge z statuscake


|status cake|

.. |status cake| image:: https://app.statuscake.com/button/index.php?Track=rHIYbOfvja&Days=1&Design=1
   :target: https://app.statuscake.com/UptimeStatus.php?tid=3999776
