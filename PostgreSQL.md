# install postgresql
brew install postgresql

# run
brew services start postgresql

# sql
psql -l # list all databases
creatdb dbname # create a database
createdb -h localhost -p 5432 UserDB # create a database on localhost:5432
dropdb dbname # drop a database
