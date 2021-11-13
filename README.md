# install

u need mongoUrl correct in config.js


and Roles collection before start u need insert document {"value":"USER"} for default user role.

# registration
POST http://localhost:5000/auth/registration


{
username: "username",
password: "password"
}

# login
POST http://localhost:5000/auth/login


{
username: "username",
password: "password"
}
return {token: "<HERE_TOKEN>"}

# getUsers
ATTTENTION: only for role "ADMIN"


NEED: bearer token from login for exactly


in headers: { Authorization: "Bearer <HERE_TOKEN>"}


GET http://localhost:5000/auth/users/