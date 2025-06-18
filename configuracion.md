docker pull postgres:17.5-alpine3.22

docker run --name postgres17 -p 5433:5432 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=secret -d postgres:17.5-alpine3.22

docker exec -it postgres17 psql -U root

brew install golang-migrate

migrate -version

migrate create -ext sql -dir db/migration -seq init_schema

createdb --username=root --owner=root simple_bank
