### Launch

```
make docker run
```
available on http://localhost:9000

### Restart

```
./compose.py latest restart
```

### Stop

```
./compose.py latest srm
```
Shortcut for stop and rm

### Commands

#### Create User
```
curl -H "Content-Type: application/json" -X POST -d '{"email":"test@test.com","password":"12345678"}' http://localhost:9000/auth/
```

#### Sign in
```
curl -v -H "Content-Type: application/json" -X POST -d '{"email":"test@test.com","password":"12345678"}' http://localhost:9000/auth/sign_in
```

#### Validate token
```
curl -v -H "Content-Type: application/json" -X POST -d '{"access-token":"lokCml393J_bvUZKvvZK_g","uid":"test@test.com"","client":"iZBty-kK5VjhJJyQc6ch-A"}' http://localhost:9000/auth/sign_in
```
