# Используем официальный образ Node.js
FROM node:alpine

# Определяем рабочую директорию внутри контейнера, куда будут загружены файлы
WORKDIR /time-app

# Копируем файлы зависимостей в контейнер
COPY package.json package-lock.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код приложения в контейнер
COPY ./src ./src
COPY index.html ./
COPY vite.config.js ./

# Открываем порт для приложения
EXPOSE 8954

# Устанавливаем команду по умолчанию для запуска dev-сервера
CMD ["npm", "run", "dev"]
