
# Chatbot with ChatGPT for Telegram built with Golang

This is a Telegram bot powered by ChatGPT and Golang. It uses OpenAI's GPT-3 to generate real-time responses to user messages.

## Prerequisites
For this application, ensure these are installed

- Go

## Features
- Real-time generation of human-like responses using the ChatGPT API
- Persisting of user conversations using sqlite
- Support for Telegram
- Go-based for efficient performance

To use the bot, create a bot on Telegram via [BotFather framework](https://t.me/botfather). Obtain an API token, and an [API key from OpenAI](https://platform.openai.com/account/api-keys)

A sample `.env` file
```.env
TELEGRAM_API_KEY=""
OPENAI_TOKEN=""
RETAIN_HISTORY="false"
```
`RETAIN_HISTORY="true"` includes past conversations with current text as seen [here](https://platform.openai.com/docs/guides/chat/introduction). But when false, it sends only the prompt and current user's text, reducing the tokens sent per request.

You should create a `prompt.txt` or rename the example file
```sh
$ mv prompt.example.txt prompt.txt
```
This helps customize the bot's responses.

## Example chat conversation
![Example Image](./screenshots/scrnsht1.png "A sample conversation")

## Installation
To install, follow these steps:

```sh
git clone github.com/ruibing1/chatbot-tele-gpt.git
```
Then, navigate to the project directory:
```sh
cd chatbot-tele-gpt
```
Finally, build:
```sh
go build -o /opt/chatbot-tele-gpt
```

## How to contribute
To contribute, follow these steps:

- Fork the repository.
- Create a new branch (git checkout -b <branch-name>).
- Make and commit your changes (git commit -am "<commit-message>").
- Push to the branch (git push origin <branch-name>).
- Open a new PR

## License
Project is under the MIT License. View the LICENSE file for the specifics

## Useful links
- [Go Documentation](https://golang.org/doc/)
- [Telegram Bot API](https://core.telegram.org/bots/api)