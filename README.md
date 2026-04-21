# Telegram Discussion Notifications

[🇷🇺 Русский](#русский) | [🇬🇧 English](#english)

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

<a name="english"></a>

## 🇬🇧 English

GitHub Action for sending notifications about events in GitHub Discussions to a Telegram chat.

### Features
- Notifications for new discussions and comments.
- Support for event editing notifications (configurable).
- Display of the first 255 characters of the message body.
- Support for multiple languages (EN, RU).
- Username mapping from GitHub to Telegram.
- Support for Telegram supergroup topics (Thread ID).
- Option to ignore bot actions.

### Usage

```yaml
- name: Telegram Notification
  uses: ai-agent-net/discussions-tg-notifications@main
  with:
    bot_token: ${{ secrets.TELEGRAM_BOT_TOKEN }}
    chat_id: ${{ secrets.TELEGRAM_CHAT_ID }}
    events: "created, edited"
    language: "en"
```

### Inputs

| Parameter | Description | Required | Default |
|-----------|-------------|----------|---------|
| `bot_token` | Telegram Bot Token | Yes | - |
| `chat_id` | Telegram Chat ID | Yes | - |
| `message_thread_id` | Topic ID for supergroups | No | - |
| `user_map` | Mapping `gh_user=tg_user`, one per line | No | - |
| `ignore_bots` | Ignore actions performed by bots | No | `true` |
| `language` | Notification language (`en`, `ru`) | No | `ru` |
| `events` | Comma-separated list of events (`created`, `edited`) | No | `created` |

---

<a name="русский"></a>

## 🇷🇺 Русский

GitHub Action для отправки уведомлений о событиях в GitHub Discussions в Telegram чат.

### Возможности
- Уведомления о новых обсуждениях и комментариях.
- Поддержка уведомлений о редактировании (настраивается).
- Отображение первых 255 символов тела сообщения.
- Поддержка нескольких языков (EN, RU).
- Маппинг имен пользователей GitHub -> Telegram.
- Поддержка топиков в супергруппах Telegram (Thread ID).
- Возможность игнорировать действия ботов.

### Использование

```yaml
- name: Telegram Notification
  uses: ai-agent-net/discussions-tg-notifications@main
  with:
    bot_token: ${{ secrets.TELEGRAM_BOT_TOKEN }}
    chat_id: ${{ secrets.TELEGRAM_CHAT_ID }}
    events: "created, edited"
    language: "ru"
```

### Входные параметры

| Параметр | Описание | Обязателен | По умолчанию |
|----------|----------|------------|--------------|
| `bot_token` | Токен Telegram бота | Да | - |
| `chat_id` | ID чата Telegram | Да | - |
| `message_thread_id` | ID темы (Thread ID) для супергрупп | Нет | - |
| `user_map` | Маппинг `gh_user=tg_user`, по одному на строку | Нет | - |
| `ignore_bots` | Игнорировать действия ботов | Нет | `true` |
| `language` | Язык уведомлений (`en`, `ru`) | Нет | `ru` |
| `events` | Список событий через запятую (`created`, `edited`) | Нет | `created` |
