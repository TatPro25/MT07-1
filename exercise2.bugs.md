## Задание №2. Составление тест-плана
### Баг-репорты тестового набора Fake REST API
___
> **Баг-репорты на раздел "CoverPhotos"**

## ID 1. Test-case ID: 62. Неверный HTTP статус ответа  

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. Заполнить тело запроса эндпоинта POST с id 0
 2. Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/Activities
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200 Ок  

*Окружение:*  
Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)

## ID 2. Test-case ID: 121. Неверный HTTP статус ответа   

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*  
Minor 
  
*Шаги для воспроизведения:*  

 1. Ввети значение id 0
 2. Отправить GET запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/0
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP Status: 404 Error: Not Found

*Фактический результат:*  
HTTP статус: 200 Ок  

*Окружение:*  
Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)


## ID 3. Test-case ID: 122. Неверный HTTP статус ответа  

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*  
Minor 
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID -7
 2. Отправить GET запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/-7
 3. Проверить код состояния

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*   
HTTP статус: 200 Ок  

*Окружение:*  
Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)


## ID 4. Test-case ID: 120. Неверный HTTP статус ответа     

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*  
Minor  
  
*Шаги для воспроизведения:*  

 1. Оставить поле для ввода id пустым
 2. Отправить POST запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
 3. Проверить код состояния

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request  

*Фактический результат:*  
HTTP статус: 200 Ок 

*Окружение:*  
Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)


## ID 5. Test-case ID: 123. Неверный HTTP статус ответа  

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*  
Critical   
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 0
 2. Отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/0
 3. Проверить код состояния

 *Ожидаемый результат:*  
  HTTP статус: 400 Error: Bad Request

*Фактический результат:*  
  HTTP статус: 200 Ок 

*Окружение:*  
  Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)

## ID 6. Test-case ID: 124. Неверный HTTP статус ответа  

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*  
Critical   
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID -8
 2. Отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/-8
 3. Проверить код состояния

 *Ожидаемый результат:*  
  HTTP статус: 400 Error: Bad Request

*Фактический результат:*  
  HTTP статус: 200 Ок 

*Окружение:*  
  Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)

## ID 7. Test-case ID: 126. Неверный HTTP статус ответа  

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел CoverPhotos

*Серьезность:*  
Critical   
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 14
 2. В поле тело запроса ввести: { }
 3. Отправить PUT запрос https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/-8
 4. Проверить код состояния

 *Ожидаемый результат:*  
  HTTP статус: 400 Error: Bad Request

*Фактический результат:*  
  HTTP статус: 200 Ок 

*Окружение:*  
  Браузер Google Chrome, Версия 114.0.5735.134 (Официальная сборка), (64 бит)

>**Баг репорты раздела "Activities"**

## ID 8. Test-case ID: 18. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 0
 2. Запрос GET отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities/0
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 404 Error: Not Found  

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 9. Test-case ID: 110. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID -14
 2. Запрос GET отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities/-14
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 404 Error: Not Found  

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 10. Test-case ID: 4. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. В поле тело запроса ввести:
 ```
 { 
    "id": -14,
    "title": "Наименование",
    "dueDate": "2023-06-26T12:02:24.158Z",
    "completed": true
  } 
```
 2. Запрос POST отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200   

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 11. Test-case ID: 16. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. В поле тело запроса ввести:
 ```
  { 
    "id": 0,
    "title": "title_1",
    "dueDate": "2023-06-29T19:06:54.210Z",
    "completed": true
  }
```  
 2. Запрос POST отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200   

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 12. Test-case ID: 97. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. В поле тело запроса ввести: {}
 2. Запрос POST отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200   

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 13. Test-case ID: 8. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 2606202377
 2. В поле тело запроса ввести:
 ```
  {
    "id":12 ,
    "title": "Наименование" ,
    "dueDate": "2023-06-26T18:15:07.032Z",
    "completed": true
  }
```
 3. Запрос PUT отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities/2606202377
 4. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 404 Error: Not Found 

*Фактический результат:*  
HTTP статус: 400 Error: Bad Request   

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 14. Test-case ID: 100. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Раскрыт раздел Activities

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 14
 2. В поле тело запроса ввести: {}
 3. Запрос PUT отправить на https://fakerestapi.azurewebsites.net/api/v1/Activities/14
 4. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___
> **Баг репорты раздела "Authors"**

## ID 15. Test-case ID: 27. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Заполнить тело запроса в формате JSON
 ```
  {
   "id": 0,
   "idBook": 1,
   "firstName": "firstName_0",
   "lastName": "lastName_0"
  }
```             
 2. Запрос POST отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200   

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 16. Test-case ID: 104. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Заполнить тело запроса в формате JSON:{ }
 2. Запрос POST отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 17. Test-case ID: 114. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 0.
 2. Запрос GET отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/0
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 404 Error: Not Found 

*Фактический результат:*  
HTTP статус: 200    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 18. Test-case ID: 116. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID -14
 2. Запрос GET отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/-14
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 19. Test-case ID: 36. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 0
 2. Запрос GET отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors/0
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 404 Error: Not Found    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 20. Test-case ID: 37. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Critical  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID -2
 2. Запрос GET отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors/-2
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP статус: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 404 Error: Not Found    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

## ID 21. Test-case ID: 106. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 14
 2. В поле тело запроса ввести: {}
 3. Запрос PUT отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors/14
 4. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP Status: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)
___

# ID 22. Test-case ID: 43. Неверный HTTP статус ответа

*Предшествующие условия:*  
* Открыта страница https://fakerestapi.azurewebsites.net/index.html
* Открыта вкладка "Authors"

*Серьезность:*
Minor  
  
*Шаги для воспроизведения:*  

 1. Ввести в значение ID 2606202377
 2. Запрос DELETE отправить на https://fakerestapi.azurewebsites.net/api/v1/Authors/2606202377
 3. Проверить код состояния ответа

 *Ожидаемый результат:*  
 HTTP Status: 400 Error: Bad Request 

*Фактический результат:*  
HTTP статус: 200    

*Окружение:*  
Браузер Google Chrome, Версия 113.0.5672.127 (Официальная сборка), (64 бит)











Версия 114.0.5735.199 (Официальная сборка), (64 бит) 


