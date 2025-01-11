install_xrdp
=============

Роль устанавливает/настраивает GUI (fly - для Astra Linux; mate - для REDOS), xrdp и Яндекс браузер (яндекс браузер устанавливается толлько на Astra Linux, на REDOS необходима устанавливать руками)

Example Playbook
----------------

Including an examle of how ti use your role (for instance, with variables passed in as parameters) is always nice fore users too:

   - hosts: servers
     roles:
       - install_xrdp

Перезагрузка после установки GUI
----------------

После установки GUI сервер будет перезагружен, если сервер не надо перезагружать, то необходимо добавить тэг (если GUI уже были установлены, то перезагрузка не произойдет)

  ansible-playbook playbook.yml --skip-tags reboot
