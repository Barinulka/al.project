# Развертываение проекта
1. Клонируем репозиторий
```
git clone git@github.com:Barinulka/al.project.git
```
2. Создаем .env файл из .env-example
```
cp .env-example .env
```
3. Устанавливаем зависимости
```
coposer install
```
4. Для работы с локальной БД
   * Устанавливаем docker-compose
   * Собираем контейнер с БД из корня проекта
   ```
    docker-compose up -d
   ```
   * Применяем все миграции
   ```
   php bin/console doctrine:migrations:migrate
   ```
5. Запускаем локальный сервер symfony
    * Запуск сервера 
    ```
    symfony server:start
    ```
   * Остановка сервера
   ```
   symfony server:stop
   ```
   * Запуск сервера в фоне
   ```
   symfony serve -d
   ```