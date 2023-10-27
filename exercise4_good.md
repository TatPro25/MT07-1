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




__56 Books/GET/api/v1/Books__

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Books

__2. Ожидаемый результат:__

   Запрос успешно отправлен на сервер, HTTP код - 200 OK
   
__3. Заголовки запроса:__
 
``` 
 User-Agent: PostmanRuntime/7.32.3
 Accept: */*
Cache-Control: no-cache
Postman-Token: eb078d3f-f2aa-43bc-a218-db92c3857d79
Host: xn--zug
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

```
__4. Тело запроса:__
```
НЕТ

```

__5. Заголовки ответа:__ 

```
Date: Sun, 02 Jul 2023 12:01:25 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 8737
Connection: close
ETag: W/"2221-5jB9Tk8Aju3TGHYJ0Ei9zmGr4JI"
set-cookie: sails.sid=s%3AthcdyNlualrjT4KCfuGUsiMfu825C6_i.FtBOMFzDFdciuVBbKGp6FmkRs77%2B2tYO2X4or8kbhpk; Path=/; HttpOnly

```

__6. Тело ответа:__

```
НЕТ

```
---

__57 Books/POST/api/v1/Books{14}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books{{Books_id_plus}}

__2. Ожидаемый результат:__

404 Not Found

__3. Заголовки запроса:__
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8140168c-13f0-480b-b6c7-ca6f44464deb
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__

```
НЕТ

```

__5. Заголовки ответа:__ 
```
Content-Length: 0
Date: Sun, 02 Jul 2023 12:38:01 GMT
Server: Kestrel
```

__6. Тело ответа:__

```
НЕТ

```
---

 __58 Books/POST/api/v1/Books{2606202377}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_big}}

__2. Ожидаемый результат:__

405 Method Not Allowed

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ee76152b-ac1c-4b68-867f-90fe4b9e94fe
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
```
НЕТ
```

__5. Заголовки ответа:__ 
```
Content-Length: 0
Date: Sun, 02 Jul 2023 13:12:23 GMT
Server: Kestrel
```
__6. Тело ответа:__
```
НЕТ
```
--- 





__59 Books/POST/api/v1/Books/{-14}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books/-14

__2. Ожидаемый результат:__

405 Method Not Allowed

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 1bf4934b-be53-44ad-9d28-4d5609243b59
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

__4. Тело запроса:__
```
НЕТ
```
__5. Заголовки ответа:__ 
```
Content-Length: 0
Date: Sun, 02 Jul 2023 14:14:07 GMT
Server: Kestrel
Allow: DELETE, GET, PUT
```
__6. Тело ответа:__
```
НЕТ
```
---

__60 Books/api​/v1​/Books{0}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books{{Books_id_null}}

__2. Ожидаемый результат:__

404Not Found

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2411617e-e529-473b-a173-33aef412bb1a
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

```
__4. Тело запроса:__
``` 
none
```
__5. Заголовки ответа:__ 
``` 
Content-Length: 0
Date: Mon, 03 Jul 2023 11:08:58 GMT
Server: Kestrel
``` 
__6. Тело ответа:__
``` 
none
``` 
---


__61 Books/POST/api/v1/Books/{-14}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_minus}}

__2. Ожидаемый результат:__

405Method Not Allowed

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 259f082c-2ee2-4ff0-85c1-7b342131e1bd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
none
```
__5. Заголовки ответа:__ 
``` 
Content-Length: 0
Date: Mon, 03 Jul 2023 11:15:45 GMT
Server: Kestrel
Allow: DELETE, GET, PUT
``` 
__6. Тело ответа:__
``` 
none
``` 

---
__62 Books/POST/api/v1/Books{}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{}

__2. Ожидаемый результат:__

405Method Not Allowed

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3f85847a-e9f6-47c0-ac3f-3e7825deec0c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
none
```
__5. Заголовки ответа:__ 
``` 
Content-Length: 0
Date: Mon, 03 Jul 2023 11:28:12 GMT
Server: Kestrel
Allow: DELETE, GET, PUT
``` 
__6. Тело ответа:__
``` 
none
``` 

---
__63 Books/POST/Books/api​/v1​/- none body__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_plus}}

__2. Ожидаемый результат:__

405Method Not Allowed

__3. Заголовки запроса:__
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a9ebd4fa-ffaf-48eb-af5e-de5e631f0ced
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
none
```
__5. Заголовки ответа:__ 
``` 
Content-Length: 0
Date: Mon, 03 Jul 2023 11:32:46 GMT
Server: Kestrel
Allow: DELETE, GET, PUT
``` 
__6. Тело ответа:__
``` 
none
``` 
---
__64 Books/GET/api/v1/Books{2606202377}}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books/2606202377

__2. Ожидаемый результат:__

400Bad Request

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 783bad3b-1969-4878-a593-5a443dae6f9e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6fe7a3689aae7443b692bdb6022d625b-4984c2a722ed3b46-00",
  "errors": {
    "id": [
      "The value '2606202377' is not valid."
    ]
  }
}
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 03 Jul 2023 11:34:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
``` 
__6. Тело ответа:__
``` 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f7bf41eaa118fc4a99ac9341586ec3ff-a0f04364be4bd14a-00",
    "errors": {
        "id": [
            "The value '2606202377' is not valid."
        ]
    }
}
``` 
---
__65 Books/GET/api/v1/Books/{14}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_plus}}

__2. Ожидаемый результат:__

200OK

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 56abba4e-2504-4391-ac96-9754440a11fa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
{
  "id": 14,
  "title": "Book 14",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 1400,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-06-19T09:58:03.5687099+00:00"
}
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 03 Jul 2023 11:42:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 
{
    "id": 14,
    "title": "Book 14",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 1400,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-19T11:42:33.8420958+00:00"
}
``` 
---

__66 Books/GET/api​/v1​/Books​/{-14}__

__1. URL:__ 

​https://fakerestapi.azurewebsites.net/api/v1/Books/-14{{Books_id_minus}}

__2. Ожидаемый результат:__

200OK

__3. Заголовки запроса:__
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 4dccaa49-5781-4c3f-ab49-a3b99cb7267e
```
__4. Тело запроса:__
``` 
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-f4207e992b473c428f0884c9b0f2a319-7e35f28b2930ea48-00"
}
```
__5. Заголовки ответа:__ 
``` 
cache-control: no-store
cf-cache-status: DYNAMIC
cf-ray: 7e0edf3e0e132de4-DME
content-encoding: gzip
``` 
__6. Тело ответа:__
``` 
<!DOCTYPE html>
<html>

<head>
	<meta charset="UTF-8">
	<title>Postman</title>

	<!-- New Relic Integration -->
	<script type="text/javascript" nonce="cIGMnQQ0jTQKRNcUx0P4+wfwdeGJTUBcMyULBPQCB44DRaMJ">
		;window.NREUM||(NREUM={});NREUM.init={distributed_tracing:{enabled:true,exclude_newrelic_header:true,cors_use_newrelic_header:false,cors_use_tracecontext_headers:true,allowed_origins:['https://bifrost-web-https-v4.gw.postman.co']},privacy:{cookies_enabled:false},ajax:{deny_list:["bam.nr-data.net"]}};
``` 
---

__67 Books/GET/api/v1/Books/{0}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_null}}
__2. Ожидаемый результат:__

404

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 1b220470-0de8-4988-9f2b-59284a50acb3
```
__4. Тело запроса:__
``` 
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-14a62522f9be06439701bfa03a9c594f-835e4dd36a00344a-00"
}
```
__5. Заголовки ответа:__ 
``` 
cache-control: no-store
cf-cache-status: DYNAMIC
cf-ray: 7e0edf3e0e132de4-DME
content-encoding: gzip
``` 
__6. Тело ответа:__
``` 

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-4d318a6264ddde45814da0659cd147f6-eee1df5f4cba0f4b-00"
}
``` 
---

__68 Books/PUT/api​/v1​/Books​/{14}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_plus}}

__2. Ожидаемый результат:__

200

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c7e50412-0543-4042-a07e-cbb52316c49f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 

    "id": 14,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-03T09:59:23.591Z"
}
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 03 Jul 2023 11:47:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 
{
    "id": 14,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-03T09:59:23.591Z"
}
``` 

__69 Books/PUT/api/v1/Books/{-14}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_minus}}

__2. Ожидаемый результат:__

200

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 4fcfac46-a3e2-48c8-9fa4-bf20cb94de60
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
{
  "id": -14,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-03T09:59:23.591Z"
}
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 03 Jul 2023 11:49:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 
{
    "id": -14,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-03T09:59:23.591Z"
}
``` 
---

__70 Books/PUT/api/v1/Books/{0}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_null}}

__2. Ожидаемый результат:__

200

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ccf72a99-a052-4cb8-9d34-42127604eb9d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-03T09:59:23.591Z"
}
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 03 Jul 2023 11:50:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 
{
    "id": 0,
    "title": "string",
    "description": "string",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-03T09:59:23.591Z"
}
``` 
---

__71 Books/PUT/api​/v1​/Authors​/{14 на none body}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_plus}}

__2. Ожидаемый результат:__

415

__3. Заголовки запроса:__
```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 40152519-88c7-43ed-9ea7-e6eeeb47fbd1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

```
__4. Тело запроса:__
``` 
{
  "id": 14,
  "title": "",
  "description": "",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-03T09:59:23.591Z"
}
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 03 Jul 2023 11:53:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 
{
    "id": 14,
    "title": "",
    "description": "",
    "pageCount": 0,
    "excerpt": "string",
    "publishDate": "2023-07-03T09:59:23.591Z"
}

``` 
---

__72 Books/PUT​/api​/v1​/Authors​/{14 на { }body}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_plus}}

__2. Ожидаемый результат:__

400

__3. Заголовки запроса:__
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6106aada-2cd5-4a87-a7a6-681c1e256700
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
none
```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 03 Jul 2023 11:54:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
``` 
__6. Тело ответа:__
``` 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-a6dc06d3bd468340810b7b69cdfffef3-0a091e604ffaf049-00"
}
``` 
---

__73 Books/PUT​/api​/v1​/Authors​/{14 на -14}__

__1. URL:__ 
https://fakerestapi.azurewebsites.net/api/v1/Books/14

__2. Ожидаемый результат:__

__3. Заголовки запроса:__

```
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: bdfc4405-f547-4c56-9449-f91996b21ac0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 

```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 03 Jul 2023 11:56:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 

``` 
---

__74 Books/DELETE​/api​/v1​/Books​/{26006202377}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{Books_id_big}}

__2. Ожидаемый результат:__

400 Bad Request

__3. Заголовки запроса:__
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 02c4ee8e-32fa-4b58-afd2-c6b7c3beb845
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-95be7ac13f5ba4489c319410c12b5aaa-2b129cfb1cd6ed4d-00",
  "errors": {
    "id": [
      "The value '26006202377' is not valid."
    ]
  }
}

```
__5. Заголовки ответа:__ 
``` 
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 03 Jul 2023 12:08:48 GMT
Server: Kestrel
Transfer-Encoding: chunked

``` 
__6. Тело ответа:__
``` 

    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a4a22386f93ec247a325b15637fc2a1b-d2f97a18d5133c48-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
``` 
---

__75 Books/DELETE​/api​/v1​/Books​/{14}__

__1. URL:__ 

https://fakerestapi.azurewebsites.net/api/v1/Books/{{Books_id_plus}}


__2. Ожидаемый результат:__

200

__3. Заголовки запроса:__
```
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: de65ff8b-9110-476b-a301-27b851ee7c1f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```
__4. Тело запроса:__
``` 
none
```
__5. Заголовки ответа:__ 
``` 
Content-Length: 0
Date: Mon, 03 Jul 2023 12:11:18 GMT
Server: Kestrel
api-supported-versions: 1.0
``` 
__6. Тело ответа:__
``` 
none
``` 
---
> **User**

*__1. GET ​/api​/v1​/Users__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: f4369b88-5d8c-4abc-9a68-e8063ca0f1c2\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\

__4. Тело запроса:__
```
    Отсутствует
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 17:59:55 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
...    
    {
        "id": 10,
        "userName": "User 10",
        "password": "Password10"
    }
]
```
___

*__2. POST ​/api​/v1​/Users {14}__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 8c673c75-d446-4313-b112-ea90b0342fe0\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 90\

__4. Тело запроса:__
```
[
 {
  "id": 14,
  "userName": "Антонина",
  "password": "Василькова"
 }
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 18:04:19 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
 {
    "id": 14,
    "userName": "Антонина",
    "password": "Василькова"
 }
]
```
___

*__3. POST ​/api​/v1​/Users {2606202377}__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: f89413b7-6e51-4400-a154-ef1832b61176\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 94\

__4. Тело запроса:__
```
[
 {
  "id": 2606202377,
  "userName": "Екатерина",
  "password": "Великая"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 18:08:30 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
 {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2bee5e4aac43f24b8aebcec0346ca80c-b8e1dc373c7b6441-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
]
```
___

*__4. POST ​/api​/v1​/Users {0}__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: c04568b8-544f-4355-8b41-66edfc1b9b4b\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 81\

__4. Тело запроса:__
```
[
 {
  "id": 0,
  "userName": "Янина",
  "password": "Крикливая"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 18:12:22 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
 {
    "id": 0,
    "userName": "Янина",
    "password": "Крикливая"
}
]
```
___

*__5. POST ​/api​/v1​/Users {-14}__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 6a7a1cd2-5e83-407a-b31b-52857e469044\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 87\

__4. Тело запроса:__
```
[
 {
  "id": -14,
  "userName": "Каролина",
  "password": "Душечная"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 18:15:22 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": -14,
    "userName": "Каролина",
    "password": "Душечная"
}
]
```
___

*__6. POST ​/api​/v1​/Users type__* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 418e2092-90c7-446a-a77c-b807dadda8b8\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 75\

__4. Тело запроса:__
```
[
{
  "id": 14,
  "userName": 007,
  "password": "Василькова"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 18:31:15 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-2e8b6e7927a71048ab0c98aaa8d22595-2dc3c63eaac2c446-00",
    "errors": {
        "$.userName": [
            "Invalid leading zero before '0'. Path: $.userName | LineNumber: 2 | BytePositionInLine: 15."
        ]
    }
}
]
```
___

*__7. POST ​/api​/v1​/Users JSON* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 9c3ba68f-9632-4314-b19f-31f563dbeebf\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 91\

__4. Тело запроса:__
```
[
{
  "id" = 14,
  "userName": "Антонина",
  "password": "Василькова"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 18:35:36 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4d0983a63064d84e96f3977fa313b715-bd7ce865ea9b0646-00",
    "errors": {
        "$": [
            "'=' is invalid after a property name. Expected a ':'. Path: $ | LineNumber: 1 | BytePositionInLine: 7."
        ]
    }
}
]
```
___

*__8. POST ​/api​/v1​/Users {}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 5a81187f-57e1-4c37-a487-dc749be94d5e\
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
Date: Sun, 02 Jul 2023 18:38:55 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": 0,
    "userName": null,
    "password": null
}
]
```
___

*__9. POST ​/api​/v1​/Users - none body* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 274e7621-a097-437b-b46e-1451487f3d64\
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
Date: Sun, 02 Jul 2023 18:41:25 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-bebac2fe19aa9240876ed8835deb1d76-498b30c5680e3849-00"
}
]
```
___

*__10. GET ​/api​/v1​/User​/{4}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 060e0cb2-541d-459c-abb3-cea5926105be\
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
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 18:49:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__
```
[
{
    "id": 4,
    "userName": "User 4",
    "password": "Password4"
}
]
```
___

*__11. GET ​/api​/v1​/User​/{2606202377}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
UUser-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 81c9d00c-abd0-40bc-8b7d-775270bbede1\
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
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 02 Jul 2023 18:52:39 GMT
Server: Kestrel
Transfer-Encoding: chunked

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f17bbd24e823da45b690076009e73af0-2676da50f16a784a-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
]
```
___

*__12. GET ​/api​/v1​/User​/{0}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_null}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: c0a503c6-4e3e-4dec-bb53-0dfba55bac0e\
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
Date: Sun, 02 Jul 2023 18:56:20 GMT\
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
    "traceId": "00-bb12ccb47f8e9c46949434376db7514c-f215ad393f2a0e4c-00"
}
]
```
___

*__13. GET ​/api​/v1​/User​/{-14}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: a3f3016c-6778-4972-bd47-ddc61ceeb25b\
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
Date: Sun, 02 Jul 2023 18:58:59 GMT\
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
    "traceId": "00-46b08c00c863794ea69e5031d3480947-2619dc841c5ffb46-00"
}
]
```
___

*__14. PUT ​/api​/v1​/Users​/{4}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200 OK

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 9f15fbee-24da-4e53-8d4a-fff3e64cc3cb\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 63\

__4. Тело запроса:__
```
[
{
  "id": 12,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 19:04:03 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
  "id": 12,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```
___

*__15. PUT ​/api​/v1​/Users​/{2606202377}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 32b02e47-ab4a-431f-bcd0-c0ffe7449e27\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 69\

__4. Тело запроса:__
```
[
{
  "id": 7,
  "userName": "User_7",
  "password": "Password_7"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 19:08:37 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-b17979853c6f404cbb2815d393c172bd-312b3a6e487ac54a-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
]
```
___

*__16. PUT ​/api​/v1​/Users​/{0}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 8a446042-cf97-4772-a18b-84c9e6acc676\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 62\

__4. Тело запроса:__
```
[
{
  "id": 2,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 19:18:56 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": 2,
    "userName": "Lucky",
    "password": "Bolt"
}
]
```
___

*__17. PUT ​/api​/v1​/Users​/{-14}* 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_minus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: dfba55de-d665-47b2-b63b-966eaa7a0be0\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 63\

__4. Тело запроса:__
```
[
{
  "id": 2,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 19:14:59 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": 2,
    "userName": "Lucky",
    "password": "Bolt"
}
]
```
___

*__18. PUT ​/api​/v1​/Users​/{4 на 2606202377}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type_: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 9db0c7f0-bd70-46e4-ac14-f6636f3a0929\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 71\

__4. Тело запроса:__
```
[
{
  "id": 2606202377,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 19:23:04 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-fbcf7be01909774d99137a6ca5d21885-6f8db4111dfe9143-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
]
```
___

*__19. PUT ​/api​/v1​/Users​/{4 на 0}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 799fbd26-3ac4-4166-9bd8-6aca5c561218\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 62\

__4. Тело запроса:__
```
[
{
  "id": 0,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 19:26:56 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": 0,
    "userName": "Lucky",
    "password": "Bolt"
}
]
```
___

*__20. PUT ​/api​/v1​/Users​/{4 на -14}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 70f5e696-caae-4424-b19a-641fa43fc455\
Host: fakerestapi.azurewebsites.net\
Accept-Encoding: gzip, deflate, br\
Connection: keep-alive\
Content-Length: 64\

__4. Тело запроса:__
```
[
{
  "id": -14,
  "userName": "Lucky",
  "password": "Bolt"
}
]
```

__5. Заголовки ответа:__ \
Content-Type: application/json; charset=utf-8; v=1.0\
Date: Sun, 02 Jul 2023 19:30:03 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": -14,
    "userName": "Lucky",
    "password": "Bolt"
}
]
```
___

*__21. PUT ​/api​/v1​/Users​/{4 на {} body}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 400 Bad Request

__3. Заголовки запроса:__\
Content-Type: application/json\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 4bb71590-b03e-4976-9502-a709be61d3ab\
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
Date: Sun, 02 Jul 2023 19:32:46 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
{
    "id": 0,
    "userName": null,
    "password": null
}
]
```
___

*__22. PUT ​/api​/v1​/Users​/{4 на none body}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 415 Unsupported Media Type

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Postman-Token: 1d32726b-708a-4a6b-b28f-ea2266eb21e8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Length: 0

__4. Тело запроса:__
```
[
none
]
```

__5. Заголовки ответа:__ \
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 19:36:02 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-b2891b22767a2541928735b3156d40af-a10e596970f9cd4e-00"
}
]
```
___

*__23. DELETE ​/api​/v1​/Users​/{4}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_plus}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: c648132b-1997-4236-bfa6-6b7fd82e4577\
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
Date: Sun, 02 Jul 2023 19:39:55 GMT\
Server: Kestrel\
api-supported-versions: 1.0\

__6. Тело ответа:__
```
[
none
]
```
___

*__24. DELETE ​/api​/v1​/Users​/{2606202377}* 

__1. URL:_  
https://fakerestapi.azurewebsites.net/api/v1/Users/{{Users_id_big}}

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, ожидаемый HTTP код - 415 Unsupported Media Type

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3\
Accept: */*\
Postman-Token: 5baae097-88d7-4b5e-906d-127dc81efed6\
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
Content-Type: application/problem+json; charset=utf-8\
Date: Sun, 02 Jul 2023 19:42:17 GMT\
Server: Kestrel\
Transfer-Encoding: chunked\

__6. Тело ответа:__
```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-73bc1f0d916644479e5f7424f59e2379-80558ae00245424e-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}
]
```
---
__1. GET​/api​/v1​/CoverPhotos__ 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 78ceb31a-89ae-4c94-b18b-34f89f5470e4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```

отсутствует тело запроса

```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 12:48:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    ...
     {
        "id": 200,
        "idBook": 200,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
    }
]
```
POST ​/api/v1/CoverPhotos




__2. POST ​/api/v1/CoverPhotos{14}__ 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__\

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 78ceb31a-89ae-4c94-b18b-34f89f5470e4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
  {
  "id": 14,
  "idBook": 234,
  "url": null
}
]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 12:48:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```

отсутствует тело ответа

```



__3. POST ​/api/v1/CoverPhotos{0}__ 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__


Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
  {
  "id": 0,
  "idBook": 234,
  "url": null
}
]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```

отсутствует тело ответа

```

__4. POST ​/api/v1/CoverPhotos{-14}__ 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
  {
  "id": -14,
  "idBook": 234,
  "url": null
}
]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```

отсутствует тело ответа

```

__5. POST ​/api/v1/CoverPhotos{2606202377}__ 

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
  {
  "id": 2606202377,
  "idBook": 234,
  "url": null
}
]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


__6. Тело ответа:__

```

отсутствует тело ответа

```

__6. POST ​/api/v1/CoverPhotos  -JSON__

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
  {
   id=14,
  "idBook": 234,
  "url": null
}
]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


__6. Тело ответа:__

```

отсутствует тело ответа

```


__7. POST ​/api/v1/CoverPhotos {}__

__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
  {}
]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


__6. Тело ответа:__

```

отсутствует тело ответа

```


__8.POST ​/api/v1/CoverPhotos (none_body)__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[ ]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


__6. Тело ответа:__

```

отсутствует тело ответа

```

__9.POST ​/api/v1/CoverPhotos  (incorrect data)__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

__2. Ожидаемый результат:__

HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
[
    {
  "id": 14,
  "idBook": буквы,
  "url": null
}
 ]
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0


__6. Тело ответа:__

```

отсутствует тело ответа

```


__10.GET/api​/v1​/CoverPhotos​/books​/covers​/{14}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/14

__2. Ожидаемый результат:__


    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
    {
        "id": 14,
        "idBook": 14,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 14&w=250&h=350"
    }
]

```



__11.GET/api​/v1​/CoverPhotos​/books​/covers​/{0}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/0

__2. Ожидаемый результат:__


    HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
тело ответа отстуствует
```


__12.GET/api​/v1​/CoverPhotos​/books​/covers​/{2606202377}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/2606202377

__2. Ожидаемый результат:__


    HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5c334ee58997154b82ccdf1e8e6b5c5c-a1e5df320007cb45-00",
  "errors": {
    "idBook": [
      "The value '2606202377' is not valid."
    ]
  }
}]
```

__12.GET/api​/v1​/CoverPhotos​/books​/covers​/{-14}__
__1. URL:__  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/-14

__2. Ожидаемый результат:__


    HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
отсутствует тело ответа
```

__13.GET​/api​/v1​/CoverPhotos​/{14}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
  "id": 14,
  "idBook": 14,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 14&w=250&h=350"
}
]

```

__14.GET​/api​/v1​/CoverPhotos​/{0}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/0

__2. Ожидаемый результат:__


 
    HTTP статус: 404 Error: Not Found

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-84eb096ceea2cb4fb656445233de8155-d19aa2ffb8528d42-00"
}
]

```

__15.GET​/api​/v1​/CoverPhotos​/{-14}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/-14

__2. Ожидаемый результат:__


 
    HTTP статус: 404 Error: Not Found

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-a834e5b25429e245b142fa8a60970599-ef80f25e26edc747-00"
}
]

```




__16.GET​/api​/v1​/CoverPhotos​/{2606202377}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/2606202377

__2. Ожидаемый результат:__
 
    HTTP статус: 404 Error: Not Found

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
отсутствует тело запроса
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5c29812bafb86d4fae0e9ec6f2afa7b0-a966a128cc6ec04a-00",
  "errors": {
    "id": [
      "The value '2606202377' is not valid."
    ]
  }
}
]
```

__17.PUT​/api​/v1​/CoverPhotos​/{14}__
__1. URL:__  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


    Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  "id": 14,
  "idBook": 123,
  "url": "string"
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-4433bd5e862d85488f5b36b648b323c8-6c5f3862c9b5004d-00"
}
]

```

__18.PUT​/api​/v1​/CoverPhotos​/{-14}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/-14

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  "id": -14,
  "idBook": 123,
  "url": "string"
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-4d0d53dc13c88b44bd57067e4fe395fd-16504d7943e27840-00"
}
]

```


__19.PUT​/api​/v1​/CoverPhotos​/{0}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/0

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  "id": 0,
  "idBook": 123,
  "url": "string"
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-417365fbd304e240ba860450a00f5251-fc08d1ccc11b9f41-00"
}
]

```

__20.PUT​/api​/v1​/CoverPhotos​/{2606202377}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/2606202377

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  "id": 2606202377,
  "idBook": 123,
  "url": "string"
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-260f858baf6e0541a790fe1f61a89ef2-03b633181d523246-00"
}
]

```



__21.PUT ​/api​/v1​/CoverPhotos​/{14 на none body}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```

```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-7d48b2785f01534c99911ff6fe7ad3b6-10def25792b3854e-00"
}
]

```


__22.PUT ​/api​/v1​/CoverPhotos​/{14 -JSON}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  id=14,
  "idBook": 123,
  "url": "string"
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
    {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-2e0c503a90387d42bc7feb31360d98c3-6712404557309646-00"
}
]

```

__23.PUT ​/api​/v1​/CoverPhotos​/ 14 на {}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{ }
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
   {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-fdb9d0b57b26e84ca7ffad8ba2b3bb0c-870ef23288919642-00"
}
]

```


__24.PUT ​/api​/v1​/CoverPhotos​/ {14}  (incorrect data)__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  id=14,
  "idBook": буквы,
  "url": null
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
   {
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-209f259080837041b95f6a584dbc65da-56c4c6994b8c144b-00"
}
]

```


__25.PUT ​/api​/v1​/CoverPhotos​/ {14}  ( id empty)__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-85c3e31801fb654783abc930cb607d3b-be9d5040c9069748-00",
  "errors": {
    "$.id": [
      "',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 7."
    ]
  }
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
[
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.13",
    "title": "Unsupported Media Type",
    "status": 415,
    "traceId": "00-22a974550349524ea42423805494fba6-679bf0fe63b67146-00"
}
]

```


__26.DELETE ​/api​/v1​/CoverPhotos​/ {14}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14

__2. Ожидаемый результат:__


   Запрос успешно отправлен на сервер, HTTP код - 200 OK

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
тело запроса отсутствует
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
тело ответа отсутствует

```



__27.DELETE ​/api​/v1​/CoverPhotos​/ {14}__
__1. URL:__  
https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/2606202377

__2. Ожидаемый результат:__


   HTTP статус: 400 Error: Bad Request

__3. Заголовки запроса:__

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f66ce6cb-ed8d-422d-ac83-2a102ff47199
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

__4. Тело запроса:__
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-e78039cd1679014c903d4160beedd492-151f3be024251145-00",
  "errors": {
    "id": [
      "The value '2606202377' is not valid."
    ]
  }
}
```

__5. Заголовки ответа:__ 

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 02 Jul 2023 13:38:34 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

__6. Тело ответа:__

```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8d90d5c082bc5048a1bc90f175e1fdfa-8ba660d9e0e88b42-00",
    "errors": {
        "id": [
            "The value '2603202377' is not valid."
        ]
    }
}

```
