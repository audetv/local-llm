# local-llm
ollama ai local

### Запуск Ollama локально на своем компьютере. 

С сайта https://ollama.com/ скачиваем ollama. \
На сайте доступны версии для различных операционных систем. \
Выбираем и скаичваем для своей операционной системы, например:
```
Download Ollama
Download for Windows
```
Запускаем загруженный файл OllamaSetup.exe

<details><summary>Download Ollama</summary>
<p>

![2024-11-14_16-20-15](https://github.com/user-attachments/assets/8ae244ca-cbcc-4f16-b8ba-6ea285c78383)

</p>
</details>

После установки ollama необходимо скачать и установить какую либо LLM модель, например можнов воспользоваться последней версией на ноябрь 2024 llama3.1:latest \
https://ollama.com/library/llama3.1 

Запустите консоль windows cmd и выполните команду \
```ollama run llama3.1``` 
Будем произведено скаивание моджели, модель «весит» 4.7GB, дождитесь завершения установки. посел завершения опявиться окно диалога.

<details><summary>ollama run</summary>
<p>

![2024-11-14_16-42-23](https://github.com/user-attachments/assets/18ebb523-f133-4999-a048-cdcb87b1b0f6)

</p>
</details>

Уже можно рабоать с моделью в этом режиме прямо в консоли. Но для удобства работы, можно установить веб-интрфейс. \
Для этого надо выйти из режима диалога с моделью, наберите \
```/bye ```

Далее скачиваем и устанавливаем докер для вашей опреационной системы. \
https://www.docker.com/ \
Если докер уже установлен пропускем этот шаг и приступаем к установке программного интерфейса для моделей LLM (ИИ)

Запускаем команду для запуска крнтейнеров openwebui в консоли вашей wsl (для windoiws)
```
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```
https://docs.openwebui.com/#quick-start-with-docker--recommended 

Дожидаемся завершения установки контейнеров. 

Заходим в докер, внизу в трее windows есть иконка докера, нажимаем на нее, открывается докер, находим в списке контейенров \
```open-webui``` \
Нажимаем в колонке Port(s) на ссылку 3000:8080 

Так же можно сразу в брузере набрать адрес: http://localhost:3000 

Регистрируемся, вводим имя, email и задаем пароль, после регистрации попадаем в программу.

Выбираем в правом верхнем углу модель llama3.1:latest

<details><summary>llama3.1:latest</summary>
<p>

![2024-11-14_11-56-31](https://github.com/user-attachments/assets/9ddeb16a-7f5b-40b2-9dab-c1d9dc3756e7)


</p>
</details> 

Теперь можно задавать вопросы и работать с ollama как с чат ботом.
