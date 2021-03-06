## Как добавить свой совет/трюк

- [сделайте форк](https://github.com/Imangazaliev/git-tips/network) репозитория

- установите зависимости:

```sh
  $ cd git-tips && npm install
```

**Внимание:** не думайте, что установка зависимостей является необязательной. Таким образом вы теряете преимущества от автоматической генерации README и содержания. Ваш пулл-реквест, скорее всего, не будет принят именно по этой причине.

- добавьте ваш совет/трюк в файл [tips.json](tips.json):

```js
{
    "title": <краткое-описание>,
    "description": <подробное-описание>,
    "tip": <команда>,
    "alternatives": [список альтернатив (опционально)]
}
```

Для переноса строк можно использовать управляющий символ `\n`. Двойные кавычки необходимо экранировать с помощью обратного слеша.

**Пример:**

```json
{
    "title": "Изменить сообщение последнего коммита",
    "description": "При выполнении команды откроется редактор, указанный в настройках git. Необходимо изменить текст сообщения, сохранить файл и закрыть редактор.\n\nСообщение можно указать и непосредственно при вызове команды с помощью опции `-m` (`--message`)",
    "tip": "git commit --amend\n\n# можно указать сообщение с помощью опции -m\ngit commit --amend -m \"New message\""
},
```

- cделайте коммит, пуш и отправьте пулл-реквест
