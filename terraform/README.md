# Описание работы
* Создана новая папка в Yandex Cloud, получены необходимые id
* Создание папки terraform
<mkdir terraform>
* Создан файл .gitignore с исключениями
<vim .gitignore>
* Переход в папку terraform
* Создан файл provider.tf
* Создан файл variables.tf
* Создан файл wp.auto.tfvars и в него внесены id облака, папки
* Инициализирован terraform backend
<terraform init>
* Создан файл network.tf
* Применены изменения в конфигурации командой
<terraform apply --auto-approve>
* Создан файл wp-app.tf
* Применены изменения в конфигурации командой
<terraform apply --auto-approve>
* Создан файл ld.tf
* Применены изменения в конфигурации командой
<terraform apply --auto-approve>
* Создан файл db.tf
* Применены изменения в конфигурации командой
<terraform apply --auto-approve>
* Создан файл output.tf
* Применены изменения в конфигурации командой
<terraform apply --auto-approve>
В результате выполнения получены ip адреса и имя хоста
* Произведено удаление инфрастрруктуры командой
<terraform destroy --auto-approve>
* Создан файл README.md

