# Домашнее задание: practice/rebase-playground

Ветка создана от `main` и осталась локальной, как указано в методичке. В ней созданы три коммита:

```text
5a47fee docs: explain rebase
908bd1b docs: explain merge
7425552 docs: note branch preparation
```

Для последних трёх коммитов запущен `git rebase -i HEAD~3`. Действия: `pick`, `pick`, `squash`. Объединённым коммитам задано сообщение `docs: compare merge and rebase`.

Итог:

```text
b91030b docs: compare merge and rebase
7425552 docs: note branch preparation
```

После rebase Git подтвердил ту же файловую версию дерева (`298f218b0911a08220b4abfe142229e232567b12`), что была до преобразования истории. Ветка `practice/rebase-playground` не отправлялась на GitHub.

## Команды для повторной проверки

```bash
git switch practice/rebase-playground
git log --oneline -3
git switch main
git log --oneline main..practice/rebase-playground
```

Для отчёта также сохранена расшифровка реального вывода команд в `practice_02/rebase_exercise.md`; скриншот экрана не подменён сгенерированным изображением.
