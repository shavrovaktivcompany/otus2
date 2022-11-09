# Описание работы
* Создана новая папка в Yandex Cloud, получены необходимые id
* Установлены файлы для поддержки языка программирования Golang по инструкции https://golang.org/doc/install
* Cоздан новый git branch
<git switch -c ansible>
* Создан файл .gitignore с исключениями для поддержки Golang
<vim .gitignore>
* Переход в папку terraform
* Отредактирован файл outputs.tf
* В папке terraform создана папка test
<mkdir test>
* Осуществлен переход в папку test
* Создан файл end2end_test.go
* Инициализирован модуль Go
<go mod init test>
* Удостоверились, что в каталоге появился файл go.mod командой
<head go.mod>
* Файл end2end_test.go обновлен необходимыми командами
* Необходимые зависимости скачиваются командой
<go get github.com/gruntwork-io/terratest/modules/terraform>
<go mod vendor>
* Запускается тест с указанием таймаута для тестирования
<go test -v ./ -timeout 30m -folder 'folder-id'>
* Обновлен файл end2end_test.go для поддержки разных стадий тестирования
<go mod vendor>
* Повторно запускается тест с указанием таймаута для тестирования
<go test -v ./ -timeout 30m -folder 'folder-id'>
* Выполним только стадию создания инфраструктуры, установив переменные
<export SKIP_validate=true>
<export SKIP_teardown=true>
И запустим команду
<go test -v ./ -timeout 30m -folder 'folder-id'>
* Для запуска только стадии validate выполняем команды
<export SKIP_setup=true>
<unset SKIP_validate>
Это позволяет сократить время цикла тестирования
* Обновлен файл end2end_test.go для поддержки разных стадий тестирования
* Снова запустим тестирование командой
<go test -v ./ -timeout 30m -folder 'folder-id'>
* Снова обновляем файл end2end_test.go для поддержки передачи приватного ключа в terratest
* После добавления новой библиотеки выполним
<go mod vendor>
* Запустим тестирование с указанием приватного ключа
<go test -v ./ -timeout 30m -folder 'folder-id' -ssh-key-pass '/home/user/.ssh/id_ed25519'>
* Удалим текущую инфраструктуру установкой переменной
<unset SKIP_teardown>
и выполним команду еще раз для удаления текущей инфраструктуры
<go test -v ./ -timeout 30m -folder 'folder-id' -ssh-key-pass '/home/user/.ssh/id_ed25519'>
* Выполним запуск полного цикла тестов с самого начала
<unset SKIP_setup>
<go test -v ./ -timeout 30m -folder 'folder-id' -ssh-key-pass '/home/user/.ssh/id_ed25519'>
