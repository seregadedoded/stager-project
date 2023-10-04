

#системное 
- Написанные за сегодня заметки в daily note
```dataview
LIST without id dateformat(date(file.ctime),"HH:mm") + " " + file.link from "/" and -#дневник 
where file.cday = this.file.day
SORT file.ctime ASC
```

- все ссылки на эту заметку
```dataview
list where contains(file.outlinks, this.file.link) AND file.name != this.file.name sort file.ctime desc
```
- все заметки с определенным тэгом
```dataview
LIST
FROM #системное  AND -#дневник
```
- для проставления текущей даты и времени 
  [[<% tp.file.creation_date("YYYY-MM-DD") %>]] <% tp.file.creation_date("HH:mm") %>
















## Связанные заметки

