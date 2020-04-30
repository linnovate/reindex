# reindex

# Reindex Project Integration
- Generic Reindex (Core)
- Api Modules (Plugins & Themes)
- Wordpress
- React
- sqldump.sql (Local Environment SQL)
- Nginx


## How to download and start
```

git clone git@github.com:linnovate/reindex.git
cd reindex
git submodule update --init --force --recursive --checkout
npm install?
docker-compose up -d --build


### TODO
docker cp sqldump.sql reindex_mysql:/
docker exec -it reindex_mysql bash <-- Be in the mysql container
mysql -u reindex -p <-- enter the password
~~~~~IN MYSQL SHELL~~~~~
create database reindex;
~~~~~GET OUT OF MYSQL SHELL~~~~~~

mysql -u reindex -p reindex < sqldump.sql

~~~~~~~GET OUT OF THE MYSQL CONTAINER~~~~~~~
```

And basically that's it , you are ready to go:
```
http://localhost:8080/ <- wordpress hosted by nginx

http://localhost:5858/ <- ui(React) as spa

http://localhost:8080/graphql <- graphql and graphql playground
```
