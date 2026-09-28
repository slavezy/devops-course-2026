# Практическая работа №1: настройки и результаты

Дата проверки: 28 сентября 2026 года.

Студент: Асаков Вячеслав, ЭФБО-08-24.

## Задание 1. Git

- Установлен Git `2.51.0.windows.1`.
- Имя автора коммитов: `slavezy`.
- Email: `asakov07@gmail.com` (исправлен в глобальных и локальных настройках).
- Редактор сообщений коммитов: `code --wait`.
- Установлен VS Code `1.137.0`.

Команды для повторной проверки:

```bash
git --version
git config --get user.name
git config --get user.email
git config --get core.editor
```

## Задание 2. GitHub и SSH

Аккаунт: [slavezy](https://github.com/slavezy). Использован существующий ключ Ed25519. Аутентификация проверена командой `ssh -T git@github.com`; сервер подтвердил вход пользователя `slavezy`.

Порт 22 не ответил за время проверки, поэтому в пользовательском файле `~/.ssh/config` настроено подключение через порт 443:

```sshconfig
Host github.com
    HostName ssh.github.com
    Port 443
    User git
```

Ключ сервера для этого адреса добавлен в `known_hosts` по официально опубликованному ключу GitHub. Приватный ключ в репозиторий не включается.

Источники: [SSH через порт 443](https://docs.github.com/en/authentication/troubleshooting-ssh/using-ssh-over-the-https-port), [ключи сервера GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints).

## Задание 3. Первый репозиторий

Репозиторий: [devops-course-2026](https://github.com/slavezy/devops-course-2026).

Удалённый адрес `origin`: `git@github.com:slavezy/devops-course-2026.git`.

Файл `about_me.md` содержит ФИО, группу и список технологий. Файл `goals.md` содержит три конкретные цели на семестр.

В истории сохранены отдельные коммиты:

- `e2f9983` - `Add about_me.md with student info`.
- `297d1b9` - `docs: add semester goals`.

Оба коммита отправлены в `main`. Дополнительные материалы первой работы находятся в каталоге `practice_01`.

## Домашнее задание: знакомство с Source Control

Открывать в VS Code нужно папку `devops-course-2026`, где находятся учебные файлы и собственный каталог `.git`.

Памятка для самостоятельного знакомства с интерфейсом:

1. Нажать `Ctrl+Shift+G`, чтобы открыть Source Control.
2. Проверить выбранный репозиторий и ветку `main`.
3. Раздел Changes показывает изменённые файлы; нажатие на файл открывает сравнение с сохранённой версией.
4. Кнопка `+` подготавливает изменения к коммиту (аналог `git add`). Они появляются в Staged Changes.
5. Поле сообщения и Commit создают локальный коммит. Push отправляет его на сервер; Sync Changes может также получать удалённые изменения.
6. В Source Control Graph можно посмотреть историю и убедиться, что локальная и удалённая ветки указывают на один коммит.

При чистом рабочем дереве пустой список Changes ожидаем: все правки уже сохранены. Памятка подготовлена для изучения; она не является подтверждением личного прохождения интерфейса студентом.

Источник: [документация Source Control в VS Code](https://code.visualstudio.com/docs/sourcecontrol/overview).

Ответы на шесть контрольных вопросов и подготовка устного ответа о `main` находятся в [theory.md](theory.md).
