---
title: Поддерживаемые команды
type: docs
---

# Поддерживаемые команды
Бот поддерживает следующие команды.

### /subscribe {channel}
Подписывает текущий чат на получение уведомлений от указанного канала. Подписка оформляется именно на текущий чат, а не на того пользователя который отправил сообщение. Альтернативный формат записи - /subscribe@{channel}
{{< hint info >}}
В случае, если чат для получения является группой, у бота должны быть права на отправку сообщений.
{{< /hint >}}

### /unsubscribe {channel}
Отписывает текущий чат от уведомлений. Альтернативный формат записи - /unsubscribe_{channel}

### /channels
Отображает список зарегистрированных каналов.

### /subscriptions
Отображает сведения о подписках текущего чата.