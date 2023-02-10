.PHONY: all start wait spawn stop stop-force

all: start wait spawn stop

start:
	docker-compose up -d frontend

wait:
	sleep 20

spawn: start
	-docker exec starrocks-backend mysql -vvv -hstarrocks-frontend -P9030 -uroot -e "ALTER SYSTEM ADD BACKEND 'starrocks-backend:9050'"
	docker exec -it starrocks-backend mysql -vvv -hstarrocks-frontend -P9030 -uroot

stop:
	docker-compose down

stop-force:
	docker-compose down -v
