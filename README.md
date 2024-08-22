# DevOps

Рис.1  DOCKERFILE
![изображение](https://github.com/user-attachments/assets/dfb779ca-cf26-4c62-b6d7-965ab7bdca2a)


  В DOCKERFILE перечислены требования:
  
     - Образ собирается на основе centos:7.
     - Python версии не ниже 3.7.
     - Установлены зависимости: flask flask-jsonpify flask-restful.
     - Создана директория opt/python_api.
     - Скрипт из репозитория размещён в opt/python_api.
     - Точка вызова: запуск скрипта.
    
   Так же для обеспечения общей работоспособности добавлены:

     - подмена репозитория Centos. Замена mirrorlist на vault.centos.org
    
  Рис.2  .gitlab-ci.yml
  ![изображение](https://github.com/user-attachments/assets/355e45aa-bcdf-4f4a-8565-d7b92b3c4c6b)

   В файле .gitlab-ci.yml обеспечено требование:
   
   - При комите в любую ветку должен собираться docker image с форматом имени hello:gitlab-$CI_COMMIT_SHORT_SHA .
   - Образ должен быть выложен в Gitlab registry или yandex registry.

# Product Owner

![изображение](https://github.com/user-attachments/assets/85a3f6f4-0c6e-4f98-8447-c4dfed6bc1b1)

Создана issue

# Developer

![изображение](https://github.com/user-attachments/assets/59e65ec5-5498-45f0-aaab-468edef359a8)

Создана ветка для issue.

![изображение](https://github.com/user-attachments/assets/c6899c21-ab46-4f2f-ac9a-6f135284926f)

Merge request

![изображение](https://github.com/user-attachments/assets/acf4c9b6-b9a7-4e98-83c1-c9cee25245a2)

Pipeline merge request

![изображение](https://github.com/user-attachments/assets/9d574caa-d40e-41bd-8773-466a459240fb)

Хранилище образов

# Tester

![изображение](https://github.com/user-attachments/assets/9cf93e7a-0826-44c0-987c-37f63435bd94)

Запускаем контейнер из последнего образа в хранилище, проверяем результат
