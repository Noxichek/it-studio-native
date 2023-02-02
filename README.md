# Запуск приложения IT-Studio

---
Оглавление
1) [Установка Node.Js](#1--установка-nodejs)
2) [Клонирование репозитория](#2--клонирование-репозитория)
3) [Установка WebPack](#3--установка-webpack)
4) [Установка зависимостей](#4--установка-зависимостей)
5) [Добавление команд билда в package.json](#5--добавление-команд-билда-в-packagejson)
6) [Сборка приложения](#6--сборка-приложения)
---

## 1) Установка Node.Js
<a name="1--установка-nodejs"></a>
Скачать и установить Node.JS для вашей ОС.
https://nodejs.org/en/download/
![](https://media.geeksforgeeks.org/wp-content/uploads/20190311152716/Capture120.png)

---

## 2) Клонирование репозитория
<a name="2--клонирование-репозитория"></a>
1) Открываем терминал;
2) Переходим в директорию, где будет храниться проект;
3) Прописываем команду:

```
git clone https://gitlab.com/applications3/it-studio-native.git
```


---

## 3) Установка WebPack
<a name="3--установка-webpack"></a>
В корне проекта в терминале прописываем следующие команды:

1) Инициализируем package.json: 
```
npm init -y
```

2) Устанавливаем WebPack: 
```
npm install webpack webpack-cli --save-dev
```

3) Установка WebPack Dev Server:
```
npm install webpack-dev-server --save-dev
```
---
## 4) Установка зависимостей
<a name="4--установка-зависимостей"></a>
По очереди в терминале прописываем эти команды:
```
npm install bootstrap postcss-loader autoprefixer copy-webpack-plugin html-webpack-plugin mini-css-extract-plugin css-loader file-loader url-loader sass sass-loader style-loader --save-dev
```
```
npm install @popperjs/core
```
---
## 5) Добавление команд билда в package.json
<a name="5--добавление-команд-билда-в-packagejson"></a>
Заходим в package.json и добавляем эти команды в scripts:
```
"build": "webpack",
"start": "webpack serve --mode development"
```
---
## 6) Сборка приложения
<a name="6--сборка-приложения"></a>
1) В терминале прописываем `npm run build` и ждем пока приложение соберется. После завершения в корне приложения появится папка dist.
2) В терминале прописываем `npm start`. После выполнения приложение будет доступно по хосту `http://localhost:3000/
   `
