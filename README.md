
# Socket.IO Chat

A simple chat demo for Socket.IO

## How to use

```
$ npm i
$ npm start
```

And point your browser to `http://localhost:3000`. Optionally, specify
a port by supplying the `PORT` env variable.

## Features

- Multiple users can join a chat room by each entering a unique username
on website load.
- Users can type chat messages to the chat room.
- A notification is sent to all users when a user joins or leaves
the chatroom.


# Исследование

## add user
```angular2html
Передаем аргументом имя нового пользователя, если переменная addedUser true, выходим из события,
если false, идем дальше.
Сохраняем username в сессию socket.
Прибавляем 1 к переменной addedUser.
Вызываем событие login и выводим кол-во numUsers.
Вызываем событие user joined которое выводит username и кол-во user в чат.
```

## user left
```angular2html
Логирует пользователя, который вышел, далее определяет какое сообщение добавить в историю чата,
и просто удаляет data.
```

## stop typing
```angular2html
Ждет пока мы что-то напишем. И транслируем другим пользователям действия того кто пишет.
```

## typing
```angular2html
Просто транслируем действие
```

## new message
```angular2html
Выводится информация кто и что отправил всем. 
```

## disconnect
```angular2html
При отл пользователя мы отнимаем 1 от общего кол-во и транслируем всем о выходе и запускаем событие user left.
```

## connection
```angular2html
Ставим флаг false, вызываем событие new message и транслируем всем кто и сто отправил
```

## reconnect
```angular2html
Логируем о переподключение и транслируем кто
```

## reconnect_error
```
Логируем ошибку
```

