FORMAT: 1A
HOST: http://polls.apiblueprint.org/api/

# ruLegen Django API Doc

Тестовое API на DJANGO с использованием rest-framework.

## Программы [/program]

### Список всех программ в БД [GET]

+ Response 200 (application/json)

        [
            {
                "id": 1,
                "name": "NodeJS",
                "coast": 300,
                "description": "Это runtime JS кода"
            }
        ]

### Создание новой записи в БД[POST]


+ Request (application/json)

        {
                "name": "Имя_Программы",
                "coast": 100,
                "description": "Любой текст описывающий программу"
        }

+ Response 201 (application/json)

    + Body

            {
                
            }
            

## Программа [/program/{id}]
+ Parameters
    + id (Number) - Уникальный индентификатор по которому производится поиск в БД

### Получение инфы о конкретной программе[GET]

+ Response 200 (application/json)

        [
            {
                "id":1,
                "name":"some_name",
                "coast": 33,
                "description": "some description"
        
            }
        ]
        
+ Response 404 (application/json)

        [
            {
                "status":"Falid"
            
            }
        
        ]
    
### Удаление программы из БД [DELETE]
+ Response 200 (text/plain)
      
                "deleted"
