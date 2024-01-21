# «Введение в Ansible» - Дрибноход Давид

## Основная часть

1. Попробуйте запустить playbook на окружении из `test.yml`, зафиксируйте значение, которое имеет факт `some_fact` для указанного хоста при выполнении playbook.

Ответ: some_fact = 12

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/47ce4e2d-3e34-4257-9782-1ac62c7b217e)

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на `all default fact`.

Ответ: значение хранится в файле `group_vars/all/examp.yml`

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/2312e544-6736-4ada-9ddf-fdd87b25a3f3)

3. Воспользуйтесь подготовленным (используется `docker`) или создайте собственное окружение для проведения дальнейших испытаний.

Ответ:

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/c4385b87-4871-4b86-b6ae-d2c87ddd6aad)

4. Проведите запуск playbook на окружении из `prod.yml`. Зафиксируйте полученные значения `some_fact` для каждого из `managed host`.

Ответ: Для хоста ububntu  = deb, для centos7 = el

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/2948936b-b2f0-4608-97cd-8d6185489a96)

5. Добавьте факты в `group_vars` каждой из групп хостов так, чтобы для `some_fact` получились значения: для `deb` — `deb default fact`, для `el` — `el default fact`.

Ответ: скорректировал значение в файлах group_vars/deb/examp.yml и group_vars/el/examp.yml

6.  Повторите запуск playbook на окружении `prod.yml`. Убедитесь, что выдаются корректные значения для всех хостов.

Ответ:

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/ea405482-b265-4c96-96bb-e522c6c8ec20)

7. При помощи `ansible-vault` зашифруйте факты в `group_vars/deb` и `group_vars/el` с паролем `netology`.

Ответ:

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/23559754-041f-4198-aaad-78692c3b5a49)

8. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь в работоспособности.

Овет:

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/e15d224c-8ae7-4509-9c00-0d1bb3dd37f5)

9. Посмотрите при помощи `ansible-doc` список плагинов для подключения. Выберите подходящий для работы на `control node`.

Ответ: подходящий плагин `ansible.builtin.local`

10. В `prod.yml` добавьте новую группу хостов с именем  `local`, в ней разместите localhost с необходимым типом подключения.

Ответ: 

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/fceee7cd-64f0-4395-91fe-6192b4b8e93d)

11. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь, что факты `some_fact` для каждого из хостов определены из верных `group_vars`.

Ответ:

![image](https://github.com/DrDavidN/ans08_01hw/assets/128225763/2bc3f639-59cf-4675-b748-c14b50e0e804)

12. Заполните `README.md` ответами на вопросы. Сделайте `git push` в ветку `master`. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым `playbook` и заполненным `README.md`.
13. Предоставьте скриншоты результатов запуска команд.

---
