# DevOps-CICD
Работу выполнил студент группы ИТХ-2-21 Трефилов Владимир

Ход выполнения работы:
1. Создаем репозиторий на github и клонировать его в систему
2. Создаем все необходимые файлы и тесты, запушим их в ветку main
![image](https://github.com/user-attachments/assets/c89c40b2-b9da-4f22-81e6-de4738070a1b)
3. Создаем ветку dev, переключаемся на нее
![image](https://github.com/user-attachments/assets/d1b10ca8-b8de-45c0-8a66-92a8ad816123)
4. Устанавливаем на ветку правило, чтобы пул реквест осуществлялся только после подтверждения
![image](https://github.com/user-attachments/assets/f97354bf-2399-4daa-a2e0-4e05ed2ba62e)
5. Защищаем ветку main от прямых изменений, только через merge
6. Создаем и добавляем новый сценарий
7. В изначальном коде были намеренно допущены ошибки, чтобы убедиться, что сценарий отрабатывает как нужно
![image](https://github.com/user-attachments/assets/34864630-5be9-4afc-94e3-a80ef8c166a5)
8. Для дальнейшей проверки исправляем код: меняем функцию take_five(), исправляем отступы, отключаем сигнатуры C0114, C0115, C0116.
![image](https://github.com/user-attachments/assets/25b526dd-54ab-43e0-aa77-cd4d2a2c2523)
9. После успешно пройденных тестов создаем мердж реквест и подтверждаем
10. Регистрируемся в Dockerhub и создаем репозиторий
![image](https://github.com/user-attachments/assets/33ad4269-3384-4798-aaa4-ae187bbf8e50)
11. Создаем манифесты для куберизации нашего приложения, указываем наш репозиторий на Dockerhub как источник образа
12. Куберизируем наше приложение и применяем манифесты
13. В github в секреты добавляем токен и имя пользователя из Dockerhub
14. Создаем пайплайн для сборки и публикации в Dockerhub
15. Делаем комит новых файлов и проверяем как отрабатывает наш пайплайн
![image](https://github.com/user-attachments/assets/beab1e43-fd0b-4a32-b2ee-1e12cd272759)
16. Проверяем что пайплайн положил наш новый образ в Dockerhub
![image](https://github.com/user-attachments/assets/ea615bf9-a790-4890-b85b-a257ad92fde3)
17. Устанавливаем ArgoCD, вытаскиваем стартовый пароль и логинимся в него
![image](https://github.com/user-attachments/assets/cc49ad95-9130-4204-b30c-9cff1290afe5)
18. Подключаем к Argo наш репозиторий Github с использованием приватного ключа
![image](https://github.com/user-attachments/assets/11be13f8-9650-4cfa-a269-ac0c14933281)
19. Подключаем манифесты приложения, выбираем репозиторий, указываем реквизиты кластера k8s и пространство имен
![image](https://github.com/user-attachments/assets/1cdf4edd-bbf2-4bf5-890f-1205ca52cdcd)
20. Немного меняем наше приложение и проверяем, что Argo подхватывает изменения

![image](https://github.com/user-attachments/assets/d5d051c1-0bbf-40d0-a7e1-d9ef44027956)

