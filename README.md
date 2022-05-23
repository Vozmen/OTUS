# OTUS
HomeWork
Зарегистрировался на git и vagrant
Установил vagrant
Все действия, проводимые с vagrant осуществляю через vpn
Установил packer под root, в противном случае, был permission denied на /usr/local/bin/
Установил git
Создал ssh ключ, добавил его в ssh агент на компьютере и в веб git
Клонировал репозиторий на компьютер
Применил vagrant up, зашел по ssh, проверил версию ядра
Подключил репозиторий sudo yum install -y http://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm, обновил ядро sudo yum --enablerepo elrepo-kernel install kernel-ml -y
Обновил конфигурацию загрузчика
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
Выбрал загрузку с новым ядром по-умолчанию
sudo grub2-set-default 0
Создал образ системы через packer build centos.json
В облако vagrant через cli загрузить образ не получилось, загрузил через веб (connect_nonblock': SSL_connect returned=1 errno=0 state=SSLv3/TLS write client hello: tlsv1 alert protocol version (OpenSSL::SSL::SSLError))
https://app.vagrantup.com/Vozmen/boxes/centos-7-5/versions/1.0
Скопировал созданный образ в личный репозиторий
