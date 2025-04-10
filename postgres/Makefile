docker-prune-with-volumes:
	docker system prune -af --volumes
	sudo rm -rf data
	docker volume rm $(docker volume ls)