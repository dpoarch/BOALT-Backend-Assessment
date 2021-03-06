## BOALT-Backend-Assessment


###Getting Started
To setup the following application please run the following command on your command line:

```

composer install
php artisan passport:install
php artisan migrate
php artisan serve


```

The routes for the following application:

```

POST http://127.0.0.1:8000/api/register

POST http://127.0.0.1:8000/api/login

GET http://127.0.0.1:8000/api/user

GET http://127.0.0.1:8000/api/notification/all

POST http://127.0.0.1:8000/api/notification

PUT http://127.0.0.1:8000/api/notification

DELETE http://127.0.0.1:8000/api/notification/delete/{id}

GET http://127.0.0.1:8000/api/logout

```

Some screenshot of the results:

1. Register enter the following url on postman to register http://127.0.0.1:8000/api/register the method is [POST] for the json format
```json

{
    "name":"Admin",
    "email":"admin@example.net",
    "password":"password123",
    "password_confirmation":"password123"
}

```
![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/1.JPG "Register")


2. To login enter the following url on postman http://127.0.0.1:8000/api/login the Method is [POST] and the json format(after logging in save the acess_token to a notepad)
```json

{
    "email":"admin@example.net",
    "password":"password123"
}

```

![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/2.JPG "Login")

3. Get User Information http://127.0.0.1:8000/api/user copy the acces_token and on postman navigate to Authorization and select Bearer Token and paste the following Token the method is [GET]


![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/3.JPG "User Info")



4. Get all data of Notification http://127.0.0.1:8000/api/notification/all using method of [GET]

![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/4.JPG "All Notification")


5. Create a new notification http://127.0.0.1:8000/api/notification the method is [POST] and the json format(Copy the user id on Get User Information)
```json

{
	"user_id": 1,
	"text": "My notification content"
}

```

![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/5.JPG "Create")

6. Update notification http://127.0.0.1:8000/api/notification the method is [PUT] and the json format

```json

{
	"notification_id": 4,
	"text": "Updated notification content"
}

```

![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/6.JPG "Update")

7. Delete notification http://127.0.0.1:8000/api/notification/delete/{id} the method is [DELETE] and just replace the {} as notification id

![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/7.JPG "Delete")

8. User Session Logout http://127.0.0.1:8000/api/logout the method is [GET] navigate again to Authorization and select Bearer Token


![Alt text](https://github.com/dpoarch/BOALT-Backend-Assessment/blob/main/screenshots/8.JPG "Logout user")