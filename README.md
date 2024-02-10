# hw_3.1.2
## Создание package.json.

пишем в терминале:
npm init -y

## Шаг 2: Добавление .gitignore файла для игнорирования /node_modules.

## Шаг 3: Установка и подключение Jest.

npm install --save-dev jest

## Шаг 4: Обновление package.json с данными проекта, автора и репозитория.

## package.json
{
  "name": "hw_2.4.3",
  "version": "1.0.0",
  "description": "Created jest project",
  "main": "index.js",
  "scripts": {
    "test": "jest"
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/ValeriaSpektor/hw_2.4.3.git"
  },
  "keywords": ["Node.js","jest","JavaScript","Testing"],
  "author": "Valeria Spektor",
  "license": "MIT",
  "devDependencies": {
    "jest": "^27.0.6"
  }
}
## Создаем скрипт script.js, который содержит функцию sum для сложения двух чисел.

javascript
// script.js
function sum(a, b) {
  return a + b;
}

## Добавим тесты с использованием Jest. Создаем файл script.test.js для тестов:


const { sum } = require('./script');

test('Сумма двух положительных чисел', () => {
  expect(sum(2, 3)).toBe(5);
});

test('Сумма отрицательного и положительного числа', () => {
  expect(sum(-5, 10)).toBe(5);
});

test('Сумма двух отрицательных чисел', () => {
  expect(sum(-2, -3)).toBe(-5);
});

## Затем запустите тесты с помощью команды:

npm test или npx jest
