Створюємо image
docker build -t spalamar/nodejs-app:v1 .

Запускаємо контейнер з створеного image, встановлюємо порт 80, обмеження CPU 1 ядро, memory 512mb
docker run -p 80:80 --cpus="1.0" -m 512mb spalamar/nodejs-app:v1

Пушимо image у публічний репозиторій Dockerhub
docker push spalamar/nodejs-app:v1
