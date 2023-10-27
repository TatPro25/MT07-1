## Задание №4. Тестирование API с Postman

> **Activities**

*__1. GET/api/v1/Activities__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 3cae5112-f754-4aad-8776-3f927d846e09\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive

__4. Тело запроса:__
```
    Отсутствует
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 01 Jul 2023 17:29:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__
```
[ 
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-07-01T18:29:33.8675438+00:00",
        "completed": false
    }
...    
{
        "id": 30,
        "title": "Activity 30",
        "dueDate": "2023-07-02T23:29:33.8675547+00:00",
        "completed": true
    }
]
```
___

*__2. POST​/api​/v1​/Activities{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 711f4ac3-04de-4555-8927-09935d09d78e\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 102

__4. Тело запроса:__
```
{
  "id": 14,
  "title": "string",
  "dueDate": "2023-07-01T18:39:08.100Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sat, 01 Jul 2023 18:39:33 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 14,
    "title": "string",
    "dueDate": "2023-07-01T18:39:08.1Z",
    "completed": true
}
```
___

*__3. POST​/api​/v1​/Activities{2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: c1679b8b-79bd-4435-ad5d-fb1f222a6452\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 113\

__4. Тело запроса:__
```
{
  "id": 2606202377,
  "title": "title_big",
  "dueDate": "2023-07-01T18:39:08.100Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sat, 01 Jul 2023 18:49:22 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-acf46b8a2d442242a3b14c65da9d5179-35b272468509ea4d-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```
___

*__4. POST​/api​/v1​/Activities{0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 7f09cb80-c138-4d13-82fd-a8cbcd3fd9c5\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 104\

__4. Тело запроса:__
```
{
  "id": 0,
  "title": "title_null",
  "dueDate": "2023-07-01T18:39:08.100Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sat, 01 Jul 2023 18:53:56 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 0,
    "title": "title_big",
    "dueDate": "2023-07-01T18:39:08.1Z",
    "completed": true
}
```
___

*__5. POST​/api​/v1​/Activities{-14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 649240cf-014c-4865-8590-784e684299e5\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 106

__4. Тело запроса:__
```
{
  "id": -14,
  "title": "title_big",
  "dueDate": "2023-07-01T18:39:08.100Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sat, 01 Jul 2023 19:01:23 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": -14,
    "title": "title_big",
    "dueDate": "2023-07-01T18:39:08.1Z",
    "completed": true
}
```
___

*__6. GET​/api​/v1​/Activities​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: e076f674-fb1a-4381-8231-57cc844623a6\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sat, 01 Jul 2023 19:05:56 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 14,
    "title": "Activity 14",
    "dueDate": "2023-07-02T09:05:57.1598186+00:00",
    "completed": true
}
```
___

*__7. GET​/api​/v1​/Activities​/{2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: afe97897-245d-4df5-8e58-68c37728d2ec\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sat, 01 Jul 2023 19:10:23 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-adee804e3dd4824eb5509fd26d118de3-9e2eaf3b8fad8b47-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
```
___

*__8. GET​/api​/v1​/Activities​/{0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_null}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 2ed3e23a-d2d2-4343-9294-5e90e95e686a\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8; v=1.0\
Date: Sat, 01 Jul 2023 19:14:30 GMT\
Server: Kestrel\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-45f0d977f24d204bb14f825c625d06dd-ea1d48b996d5c640-00"
}
```
___

*__9. GET​/api​/v1​/Activities​/{-14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 47e16749-24ed-4fdf-a743-bb9c888d804c\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8; v=1.0\
Date: Sat, 01 Jul 2023 19:18:10 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-7548c3abfbebca46aa41f7a8b0d4fcae-bc429100d742e744-00"
}
```
___

*__10. POST​/api​/v1​/Activities-type__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 * (Bad Request)

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 4c05ff62-d4d1-46ae-8ae2-87b7c985b16c\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 102\

__4. Тело запроса:__
```
{
  "id": 14,
  "title": 123456789
  "dueDate": "2023-07-01T18:39:08.100Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 07:24:32 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5ea5f27aa276d140a0cea074133f47b6-b8aed9ffe7bbfd48-00",
    "errors": {
        "$.title": [
            "The JSON value could not be converted to System.String. Path: $.title | LineNumber: 2 | BytePositionInLine: 20."
        ]
}
}
```
___

*__11. POST​/api​/v1​/Activities-JSON__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 415 Unsupported Media Type

__3. Заголовки запроса:__\
Content-Type: text/plain\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 1171ef6a-0e3c-4ca5-886e-3bb7eb6ea4ba\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 100\

__4. Тело запроса:__
```
{
  id= 14,
  "title": "string",
  "dueDate": "2023-07-02T06:54:34.782Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 07:26:04 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-5aa62d1715535f40a59ff543dc6c2007-b8b77755719b684f-00"
}
```
___

*__12. POST​/api​/v1​/Activities{}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 62b1dea9-47d7-41e7-8f31-8eac494f052d\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 2\

__4. Тело запроса:__
```
{}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 07:28:57 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 0,
    "title": null,
    "dueDate": "0001-01-01T00:00:00",
    "completed": false
}
```
___

*__13. POST ​/api​/v1​/Activities{none_body}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 405 (Method Not Allowed - Метод не разрешен)

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 8025272b-9866-4497-b7ac-518b3b1c49a3\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 0\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 07:10:08 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-a185725365f66b4db00c45528502682d-9a19cfe7dff3b344-00"
}
```
___

*__14. PUT ​/api​/v1​/Activities​/14__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 ОК

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: ab7b0246-895c-4607-8109-d43e93aa2cdb\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 117\

__4. Тело запроса:__
```
{
  "id": 12,
  "title": "string",
  "dueDate": "2023-07-02T07:44:55.059Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 07:46:05 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\
__6. Тело ответа:__
```
{
    "id": 12,
    "title": "Наименование",
    "dueDate": "2023-06-26T18:15:07.032Z",
    "completed": true
}
```
___

*__15. PUT ​/api​/v1​/Activities​/-14__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 ОК

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 11e1a946-ae60-4e77-9ad5-a9fa413a4731\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 117\

__4. Тело запроса:__
```
{
    "id": 12,
    "title": "Наименование",
    "dueDate": "2023-06-26T18:15:07.032Z",
    "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 07:50:11 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\
__6. Тело ответа:__
```
{
    "id": 12,
    "title": "Наименование",
    "dueDate": "2023-06-26T18:15:07.032Z",
    "completed": true
}
```
___

*__16. PUT ​/api​/v1​/Activities​/2606202377__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request


__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: a73720c9-f3a0-404a-b5af-e1c5c74170ae\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 104\

__4. Тело запроса:__
```
{
  "id": 12,
  "title": "Title_12",
  "dueDate": "2023-07-02T07:44:55.059Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 07:50:11 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\
__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-29363c3a045d014abff891e5bca1bcc8-6d7fd63380d62443-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
```
___

*__17. PUT ​/api​/v1​/Activities​/{0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_null}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 96ee956d-d861-41da-beda-df42874d72d6\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 104\

__4. Тело запроса:__
```
{
  "id": 12,
  "title": "Title_12",
  "dueDate": "2023-07-02T07:44:55.059Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 08:02:34 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 12,
    "title": "Title_12",
    "dueDate": "2023-07-02T07:44:55.059Z",
    "completed": true
}
```
___

*__18. PUT ​/api​/v1​/Activities​/{14 на 2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 248175c3-d30d-4d10-935a-d2b7dfc766f8\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 112\

__4. Тело запроса:__
```
{
  "id": 2606202377,
  "title": "Title_12",
  "dueDate": "2023-07-02T07:44:55.059Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 08:11:29 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{ 
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0db2d78d54676647a155e515e424f5d1-c350548122eb3a44-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```
___

*__19. PUT ​/api​/v1​/Activities​/{14 на -14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 72d4a46d-c303-4697-82f2-625130337838\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 105\

__4. Тело запроса:__
```
{
  "id": -14,
  "title": "Title_12",
  "dueDate": "2023-07-02T07:44:55.059Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 08:15:22 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": -14,
    "title": "Title_12",
    "dueDate": "2023-07-02T07:44:55.059Z",
    "completed": true
}
```
___

*__20. PUT ​/api​/v1​/Activities​/{14 на 0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: ccbe8767-85a8-4182-8f28-701c6a268c16\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 103\

__4. Тело запроса:__
```
{
  "id": 0,
  "title": "Title_12",
  "dueDate": "2023-07-02T07:44:55.059Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 08:19:19 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 0,
    "title": "Title_12",
    "dueDate": "2023-07-02T07:44:55.059Z",
    "completed": true
}
```
___

*__21. PUT ​/api​/v1​/Activities​/{14 на {} body}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 4f5541a6-d3e0-4133-a4ed-32466ed1e4f1\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 2\

__4. Тело запроса:__
```
{ }
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 10:18:23 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
{
    "id": 0,
    "title": null,
    "dueDate": "0001-01-01T00:00:00",
    "completed": false
}
```
___

*__22. PUT ​/api​/v1​/Activities​/{14 на none body}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 415 Unsupported Media Type

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 7762bf3d-c6e1-4337-87d3-bf7b0f6853cf\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 0\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 10:22:22 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-ae18369362d0a946a32a977d4bf5341f-44710b55e219cd4e-00"
}
```
___

*__23. PUT ​/api​/v1​/Activities​/{14} JSON__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 69162829-0bd0-46ca-a8d6-781e2913f901\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 92\

__4. Тело запроса:__
```
{
  id = 0,
  "title": null,
  "dueDate": "0001-01-01T00:00:00",
  "completed": false
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 10:28:55 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
   "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f115766f19f6164ba14dbe6ca3eb4506-ba20187e8136e24e-00",
    "errors": {
        "$": [
            "'i' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 2."
        ]
    }
}
```
___

*__24. PUT ​/api​/v1​/Activities​/{14} type__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 48b624c4-b75d-4a7a-97a5-d9e319529446\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 100\

__4. Тело запроса:__
```
{
  "id": 12,
  "title": 123456,
  "dueDate": "2023-07-02T10:28:38.448Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 10:32:52 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-287593dbf7341c4db0176242fbcbb0d3-13c4518867bef440-00",
    "errors": {
        "$.title": [
            "The JSON value could not be converted to System.String. Path: $.title | LineNumber: 2 | BytePositionInLine: 17."
        ]
    }
}
```
___

*__25. DELETE ​/api​/v1​/Activities​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: e19290fe-e8ee-4fe8-baf2-f61e3a9d0b20\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Length: 0\
Date: Sun, 02 Jul 2023 10:36:37 GMT\
Server: Kestrel\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
none
```
___

*__24. PUT ​/api​/v1​/Activities​/{14} type__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 48b624c4-b75d-4a7a-97a5-d9e319529446\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 100\

__4. Тело запроса:__
```
{
  "id": 12,
  "title": 123456,
  "dueDate": "2023-07-02T10:28:38.448Z",
  "completed": true
}
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 10:32:52 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-287593dbf7341c4db0176242fbcbb0d3-13c4518867bef440-00",
    "errors": {
        "$.title": [
            "The JSON value could not be converted to System.String. Path: $.title | LineNumber: 2 | BytePositionInLine: 17."
        ]
    }
}
```
___

*__25. DELETE ​/api​/v1​/Activities​/{2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 8898c661-f486-487f-ac44-5b6c6ea028ac\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 10:40:34 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8b9e64350e378740a5af0a12cc4af593-fa9ba0bd5f37cb45-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
```
___
*__26. DELETE ​/api​/v1​/Activities​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activites_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: e19290fe-e8ee-4fe8-baf2-f61e3a9d0b20\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Length: 0\
Date: Sun, 02 Jul 2023 10:36:37 GMT\
Server: Kestrel\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
none
```
___

> **Authors**

*__27. GET ​/api​/v1​/Authors__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 829a580d-ec4d-4d9a-911f-aa672e6bcfe9\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
none
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 11:27:20 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    }
    ...
     {
        "id": 599,
        "idBook": 200,
        "firstName": "First Name 599",
        "lastName": "Last Name 599"
    }
]
```
___

*__28. POST ​/api​/v1​/Authors {14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 34df73b8-cbaf-4783-88c5-36934f5eccc1\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 91\

__4. Тело запроса:__
```
[
 {
  "id": 14,
  "idBook": 123,
  "firstName": "Сашка",
  "lastName": "Блок"
 }
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 11:31:39 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[{
  "id": 14,
  "idBook": 123,
  "firstName": "Сашка",
  "lastName": "Блок"
}
]
```
___

*__29. POST ​/api​/v1​/Authors {2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: a361bd3c-1c94-4156-9abf-89da251906c3\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 116\

__4. Тело запроса:__
```
[
 {
  "id": 2606202377,
  "idBook": 28,
  "firstName": "Маруся",
  "lastName": "Вегетативная"
 }
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 11:36:06 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[  
 {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-60a2c74a4f087c47ab65ba9cabeb23df-9e0169bd24857d4f-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
 }
]
```
___

*__30. POST ​/api​/v1​/Authors {0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 84cd73d0-ac45-4314-a188-6aa937802660\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 97\

__4. Тело запроса:__
```
[
 {
  "id": 0,
  "idBook": 76,
  "firstName": "Евгений",
  "lastName": "Онегин"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 11:39:58 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[  
 {
  "id": 0,
  "idBook": 76,
  "firstName": "Евгений",
  "lastName": "Онегин"
 }
]
```
___

*__31. POST ​/api​/v1​/Authors {-14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 235d191f-1ca0-4a63-a37e-48e2495a06bc\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 101\

__4. Тело запроса:__
```
[
 {
  "id": -14,
  "idBook": 65,
  "firstName": "Лава",
  "lastName": "Вулканович"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 11:43:50 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[  
 {
  "id": -14,
  "idBook": 65,
  "firstName": "Лава",
  "lastName": "Вулканович"
}
]
```
___

*__32. POST ​/api​/v1​/Authors {type}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 1a72b555-b3f2-4fed-aa3a-d804144ee121\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 97\

__4. Тело запроса:__
```
[
 {
  "id": 14,
  "idBook": Good_book,
  "firstName": "Сашка",
  "lastName": "Блок"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 11:48:38 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[  
 {
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8cefcf771ca1b647b1c01db64aec839a-544207121ebf0d46-00",
    "errors": {
        "$.idBook": [
            "'G' is an invalid start of a value. Path: $.idBook | LineNumber: 2 | BytePositionInLine: 12."
        ]
    }
}
]
```
___

*__33. POST ​/api​/v1​/Authors {JSON}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 7dd0bf18-5d0e-4374-a6a9-a660c6e9501f\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 104\

__4. Тело запроса:__
```
[
 {
  "id": 14,
  "idBook"= 123,
  "firstName": "Я_гОда",
  "lastName": "Корзинкина"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 11:52:44 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
 {  
"type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-cf1338ef081b5e499bf21a9dfca0cd19-e8253d7fb9f1dd49-00",
    "errors": {
        "$": [
            "'=' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 2 | BytePositionInLine: 10."
        ]
    }
 }
]
```
___

*__34. POST ​/api​/v1​/Authors {}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 07f3c36c-00bb-4cb9-8f9e-d40fa2b72915\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 2\

__4. Тело запроса:__
```
[
 { }
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 11:55:52 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
 {
    "id": 0,
    "idBook": 0,
    "firstName": null,
    "lastName": null
}
]
```
___

*__35. POST ​/api​/v1​/Authors - none body__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 415 Unsupported Media Type

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 4498b684-72f1-44d5-a605-0b007ab1d173\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 0\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 11:58:27 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
 {
   
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-5d45e16468c5eb45816dcfb47486023c-f5051ae3f4f5054a-00"
 }
]
```
___

*__36. GET ​/api​/v1​/Authors​/authors​/books​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: ebf9a277-21b7-41af-8a26-c7bf0c8d69d6\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:02:55 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
 {
        "id": 41,
        "idBook": 14,
        "firstName": "First Name 41",
        "lastName": "Last Name 41"
    },
    {
        "id": 42,
        "idBook": 14,
        "firstName": "First Name 42",
        "lastName": "Last Name 42"
    },
    {
        "id": 43,
        "idBook": 14,
        "firstName": "First Name 43",
        "lastName": "Last Name 43"
    }
]
```
___

*__37. GET ​/api​/v1​/Authors​/authors​/books​/{0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Authors_ID_null}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 06f54b40-7e9c-40c1-9391-cb8752c3fa0d\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:33:45 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ ]
 
```
___

*__38. GET ​/api​/v1​/Authors​/authors​/books​/{-14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{Authors_ID_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: fc7f11df-7443-40f3-a03f-95f7f69432e8\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:37:19 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ ]
 
```
___

*__39. GET ​/api​/v1​/Authors​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 6812c0c9-67d3-4a1a-9bf5-2a40d08f4589\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:42:17 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
 {
    "id": 14,
    "idBook": 5,
    "firstName": "First Name 14",
    "lastName": "Last Name 14"
 }
]
 
```
___

*__40. GET ​/api​/v1​/Authors​/{2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 1ed051f6-776c-4823-9ea9-0358e40206db\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:45:24 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
 {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-6714bd462be22245acd3f7e3f79670a0-8210d2743872d345-00"
}
]
 
```
___

*__41. GET ​/api​/v1​/Authors​/{0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_null}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 056a6ef1-82de-439f-9c9a-407f4ea5029d\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:48:26 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
 {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-e04b89ce976dd9499852152c15e14de9-b6c71b253c858b47-00"
}
]
 
```
___

*__42. GET ​/api​/v1​/Authors​/{-14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: d770b259-bea7-430d-a09d-e68d009cb376\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:50:36 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
 {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-c3730e7f44662c44b5f00da52ca0ebbd-051360e002bbd644-00"
}
]
 
```
___

*__43. PUT ​/api​/v1​/Authors​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 ОК  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 5faf84ef-67c0-45da-87ec-b8b7a82b3b07\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 96\

__4. Тело запроса:__
```
[
{
  "id": 34,
  "idBook": 57,
  "firstName": "Сергей",
  "lastName": "Есенин"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:54:40 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
    "id": 34,
    "idBook": 57,
    "firstName": "Сергей",
    "lastName": "Есенин"
}
]
 
```
___

*__44. PUT ​/api​/v1​/Authors​/{2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: bcd4cbef-a848-4b7a-8b1a-019787868bcd\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 104\

__4. Тело запроса:__
```
[
{
  "id": 34,
  "idBook": 57,
  "firstName": "Сергей",
  "lastName": "Есенин"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 12:54:40 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
    "id": 34,
    "idBook": 57,
    "firstName": "Сергей",
    "lastName": "Есенин"
}
]
 
```
___

*__45. PUT ​/api​/v1​/Authors​/{0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_null}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: b9d36acf-d2d7-49f2-ba5f-7816f1dc713a\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 105\

__4. Тело запроса:__
```
[
{
  "id": 23,
  "idBook": 65,
  "firstName": "Геннадий",
  "lastName": "Де Геннин"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 14:01:42 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
    "id": 23,
    "idBook": 65,
    "firstName": "Геннадий",
    "lastName": "Де Геннин"
}
]
 
```
___

*__46. PUT ​/api​/v1​/Authors​/{-14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 3189734d-5f4f-4278-98d4-3766cca09490\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 105\

__4. Тело запроса:__
```
[
{
  "id": 23,
  "idBook": 65,
  "firstName": "Геннадий",
  "lastName": "Де Геннин"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 14:04:58 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
    "id": 23,
    "idBook": 65,
    "firstName": "Геннадий",
    "lastName": "Де Геннин"
}
]
 
```
___

*__47. PUT ​/api​/v1​/Authors​/{14 на 2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 8c03690b-8465-4f41-a39e-8f1a0763a598\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 109\

__4. Тело запроса:__
```
[
{
  "id": -2606202377,
  "idBook": 43,
  "firstName": "Олег",
  "lastName": "Петровский"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 14:08:59 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[ 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5658992c735cec43b4ced3838baf87c0-00dc3da7f0929e4d-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 19."
        ]
    }
}
]
 
```
___

*__48. PUT ​/api​/v1​/Authors​/{14 на 0}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 1c79aeda-9fe8-41bb-9612-b079896efa8e\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 91\

__4. Тело запроса:__
```
[
{
  "id": 0,
  "idBook": 78,
  "firstName": "Агний",
  "lastName": "Барто"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 14:12:19 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
  "id": 0,
  "idBook": 78,
  "firstName": "Агний",
  "lastName": "Барто"
}
]
 
```
___

*__49. PUT ​/api​/v1​/Authors​/{14 на -14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 9fb3e5fa-c73e-478c-83ea-93147e7b0eca\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 97\

__4. Тело запроса:__
```
[
{
  "id": -14,
  "idBook": 54,
  "firstName": "Самуил",
  "lastName": "Маршак"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 14:15:18 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
  "id": -14,
  "idBook": 54,
  "firstName": "Самуил",
  "lastName": "Маршак"
}
]
 
```
___

*__50. PUT ​/api​/v1​/Authors​/{14 на {}body }__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request  

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: a8b8fdb9-7dac-4dce-bc90-4c3464741b3b\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 2\

__4. Тело запроса:__
```
[
{}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 14:20:17 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
{
    "id": 0,
    "idBook": 0,
    "firstName": null,
    "lastName": null
}
]
 
```
___

*__51. PUT ​/api​/v1​/Authors​/{14 на none body }__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 415 Unsupported Media Type
 

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 404973b4-373d-4982-b5d1-78b4eb3b732f\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 0\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 14:23:17 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[ 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-45554893cc76c74ba34b84fed3b28750-8caea0b7f0834b46-00"
}
]
 
```
___

*__52. PUT ​/api​/v1​/Authors​/{14 на JSON}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request
 

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 71322afb-1466-4502-906d-16a29425cfb8\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 100\

__4. Тело запроса:__
```
[
{
  "id": 14,
   idBook = 43,
  "firstName": "Олег",
  "lastName": "Петровский"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 14:27:35 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[ 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7b5042d2065d2f41855ddf2da274a155-dc710aad976afc49-00",
    "errors": {
        "$": [
            "'i' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 2 | BytePositionInLine: 3."
        ]
    }
}
]
 
```
___

*__53. PUT ​/api​/v1​/Authors​/{14}type__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request
 

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 563d460b-4b3c-4f5a-8dda-91c74695f68d\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 84\

__4. Тело запроса:__
```
[
{
  "id": two,
  "idBook": 65,
  "firstName": "Братья",
  "lastName": "Стругацкие"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 14:32:32 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[ 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-610e6e3e1793af429952fabb16b57ff0-04cc1cd66fbace44-00",
    "errors": {
        "$.id": [
            "'two,\r\n  \"idBook\": 0,\r\n  \"firstName\": \"string\",\r\n  \"lastName\": \"string\"\r\n}' is an invalid JSON literal. Expected the literal 'true'. Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
        ]
    }
}  
]
 
```
___

*__54. DELETE ​/api​/v1​/Authors​/{14}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK
 

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 4a596f1e-e5ac-4b44-9453-08a4076494d3\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Length: 0\
Date: Sun, 02 Jul 2023 14:38:57 GMT\
Server: Kestrel\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
none
]
 
```
___

*__55. DELETE ​/api​/v1​/Authors​/{2606202377}__ * 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Authors/{{Authors_ID_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 400 Bad Request
 

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 154d923a-17db-4f10-99c5-9f22125e3f20\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Length: 0\
Date: Sun, 02 Jul 2023 14:42:03 GMT\
Server: Kestrel\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[ 
none
]
 
```
___


