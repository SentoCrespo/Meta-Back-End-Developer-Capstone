# Description
Coursera's final assignment for the "Backend Developer Capstone" part of Meta "Backend Developer Professional Certificate".


# Structure
- The `api` (backend)
- The `restaurant` (frontend) 
- The `config` (settings)

# Steps to test

- Virtual Environment + Install dependencies
- Change DB settings if needed
- Apply DB the migrations

# Environment Variables
Inside the restaurant app folder, create a file called .env with:
```jsx
USERNAME=yout_username
PASSWORD=your_password
```
Notes: 
- Replace "your_username" and "your_password" with valid data
- `django-environ` must be installed: `pipenv install`

### Endpoints for `api` app
```jsx
http:127.0.0.1:8000/api/menu-items
http:127.0.0.1:8000/api/menu-items/{menu-itemId}
http:127.0.0.1:8000/api/bookings
http:127.0.0.1:8000/api/bookings/{bookingId}
```
<br>

http:127.0.0.1:8000/api/menu-items
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves all menu items | Yes | 200 |
| POST | Creates a menu item | Yes | 201 |
<br>

http:127.0.0.1:8000/api/menu-items/{menu-itemId}
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves the menu item details | Yes | 200 |
| PUT | Update the menu item | Yes | 200 |
| PATCH | Partially update the menu item | Yes | 200 |
| DELETE | Delete the menu item | Yes | 200 |
<br>

http:127.0.0.1:8000/api/bookings
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves all bookings | Yes | 200 |
| POST | Creates a booking | Yes | 201 |
<br>

http:127.0.0.1:8000/api/bookings/{bookingId}
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves the booking details | Yes | 200 |
| PUT | Update the booking | Yes | 200 |
| PATCH | Partially update the booking | Yes | 200 |
| DELETE | Delete the booking | Yes | 200 |
<br>

### Endpoints for `djoser` app
```jsx
http://127.0.0.1:8000/auth/users/
http://127.0.0.1:8000/auth/users/me/
http://127.0.0.1:8000/auth/users/confirm/
http://127.0.0.1:8000/auth/users/resend_activation/
http://127.0.0.1:8000/auth/users/set_password/
http://127.0.0.1:8000/auth/users/reset_password/
http://127.0.0.1:8000/auth/users/reset_password_confirm/
http://127.0.0.1:8000/auth/users/set_username/
http://127.0.0.1:8000/auth/users/reset_username/
http://127.0.0.1:8000/auth/users/reset_username_confirm/
```
<br>

http://127.0.0.1:8000/auth/users/
| Method | Action | STATUS CODE | TOKEN AUTH |
| --- | --- | --- | --- |
| GET | Retrieves all users | 200 | No |
| POST | Creates a user | 201 | No |

💡 Please refer to the [Djoser documentation](https://djoser.readthedocs.io/en/latest/getting_started.html#available-endpoints) for further usage on these endpoints.
<br> <br>

### Endpoints for `simplejwt` app
```jsx
http:127.0.0.1:8000/api/token/login/
http:127.0.0.1:8000/api/token/refresh/
```
<br>

http://127.0.0.1:8000/api/token/login/
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| POST | Generates access token and refresh token | Yes | 201 |
<br>

http://127.0.0.1:8000/api/token/refresh/
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| POST | Generates a new access token | Yes | 201 |
<br>

# Testing
Each API endpoint is tested along its allowed HTTP methods.