# Самоконтроль выполненения задания

1. Где расположен файл с `some_fact` из второго пункта задания?
2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?
3. Какой командой можно зашифровать файл?
4. Какой командой можно расшифровать файл?
5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?
6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?
7. Как называется модуль подключения к host на windows?
8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh
9. Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?

## Ответ:
1. `../group_vars/all/` ;
1. `ansible-playbook -i inventory/test.yml site.yml` ;
1. `ansible-vault encrypt <файл>` ;
1. `ansible-vault decrypt <файл>` ;
1. `ansible-vault view <файл>` ;
1. Добавляется ключ `--ask-vault-pass` ;
1. `ansible_connection=winrm` ;
1. Список модулей - `ansible-doc -t connection -l`, описание модуля `ansible-doc -t connection ssh` ;
1. Параметр `- remote_user` .
