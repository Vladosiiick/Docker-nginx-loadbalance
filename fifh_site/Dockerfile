# Використовуємо офіційний образ Nginx
FROM nginx:latest

# Аргумент для передачі значення порту
ARG PORT=80

# Копіюємо наш конфігураційний файл в контейнер
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Копіюємо HTML документ в директорію, де очікується Nginx відповідно до конфігураційного файлу
COPY index.html /usr/share/nginx/html/

# Вказуємо доменне ім'я
ENV DOMAIN_NAME example5.com

# Встановлюємо порт Nginx
EXPOSE $PORT

# Запускаємо Nginx
CMD ["nginx", "-g", "daemon off;"]