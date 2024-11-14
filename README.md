# local-llm
ollama ai local

### Запуск Ollama локально на своем компьютере. 

С сайта https://ollama.com/ скачиваем ollama. \
На сайте доступны версии для различных операционных систем. \
Выбираем и скаичваем для своей операционной системы, например: \
```
Download Ollama
Download for Windows
```
Запускаем загруженный файл OllamaSetup.exe

Скаиваем и устанавливаем докер для вашей опреационной системы. \
https://www.docker.com/ \
Если докер уже установлен пропускем этот шаг и приступаем к установке программного интерфейса для моделей LLM (ИИ)

https://docs.openwebui.com/#quick-start-with-docker--recommended
Запускаем команду для запуска крнтейнеров openwebui в консоли вашей wsl (для windoiws)
```
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```
Дожидаемся завершения установки контейнеров.
Заходим в докер, внизу в трее windows есть иконка докера, нажимаем на нее, открывается докер, находим в списке контейенров \
```open-webui``` \
Нажимаем в колонке Port(s) на ссылку 3000:8080 \
Так же можно сразу в брузере набрать адрес: http://localhost:3000
Регистрируемся, вводим имя, email и задаем пароль, после регистрации попадаем в программу.
Выбираем в праволм вверхнем углу модель llama3.1:latest
<details><summary>llama3.1:latest</summary>
<p>

![2024-11-14_11-56-31](https://github.com/user-attachments/assets/9ddeb16a-7f5b-40b2-9dab-c1d9dc3756e7)


</p>
</details> 
Теперь можно задавать вопросы и рабоать с ламой кака счат ботом.
