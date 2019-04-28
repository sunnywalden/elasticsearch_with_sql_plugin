# elasticsearch_with_sql_plugin

## build image by your self

#### download node and es-sql plugin package first
wget --no-check-certificate https://nodejs.org/dist/v10.15.3/node-v10.15.3-linux-x64.tar.xz -o /tmp/node-v10.15.3-linux-x64.tar.xz
tar -jxvf /tmp/node-v10.15.3-linux-x64.tar.xz -C .

wget --no-check-certificate https://github.com/NLPchina/elasticsearch-sql/releases/download/5.6.4.0/elasticsearch-sql-5.6.4.0.zip -o /tmp/elasticsearch-sql-5.6.4.0.zip
unzip /tmp/elasticsearch-sql-5.6.4.0.zip -d .


#### build your own image
build -t sunnywalden/elasticsearch-with-sql:v0.1 .

#### taa the new version to latest
docker tag sunnywalden/elasticsearch-with-sql:v0.1 sunnywalden/elasticsearch-with-sql:latest

#### push your image to registry
docker push sunnywalden/elasticsearch-with-sql:v0.1

docker push sunnywalden/elasticsearch-with-sql:latest


### deploy by docker

you can deploy it by compose using the docker-compose with docker-compose.yml in the root directory in this project or just use docker run commmand.
