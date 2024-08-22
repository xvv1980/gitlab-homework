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
