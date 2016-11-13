Juste a couple of side notes.

#install Postgresql
 - install package (apt-get)
 - create a user by using postgresql terminal
 - configure the file config/database.yml
 - Usefull link: https://www.digitalocean.com/community/tutorials/how-to-use-postgresql-with-your-ruby-on-rails-application-on-ubuntu-14-04


#Usage of auth API
https://github.com/lynndylanhurley/devise_token_auth#usage-tldr

#Example
- Create user
curl -H "Content-Type: application/json" -X POST -d '{"email":"test@test.com","password":"12345678"}' http://localhost:3000/auth/

- Sign in (get access_token)
curl -v -H "Content-Type: application/json" -X POST -d '{"email":"test@test.com","password":"12345678"}' http://localhost:3000/auth/sign_in

- validate token
curl -v -H "Content-Type: application/json" -X POST -d '{"access-token":"lokCml393J_bvUZKvvZK_g","uid":"test@test.com"","client":"iZBty-kK5VjhJJyQc6ch-A"}' http://localhost:3000/auth/sign_in
