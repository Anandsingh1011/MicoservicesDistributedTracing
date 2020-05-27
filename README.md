## Micoservices Distributed Tracing

We will Implement Distributed Tracing in Micoservices using Zipkin, Sleuth and ELK Stack.

### Tools

- Spring Cloud Sleuth
- Zipkin
- ELK Stack ( Three open source tools — Elasticsearch, Logstash and Kibana form the ELK stack )

### Installation of tools

1) Installing Zipkin

url -sSL https://zipkin.io/quickstart.sh | bash -s

java -DSTORAGE_TYPE=elasticsearch -DES_HOSTS=http://127.0.0.1:9200 -DES_USERNAME=elastic -DES_PASSWORD=changeme -jar zipkin.jar

2) Installing ELK Stack

git clone https://github.com/deviantony/docker-elk.git

cd /docker-elk

docker-compose up -d

run 

docker ps

You’ll notice that ports on my localhost have been mapped to the default ports used by Elasticsearch (9200/9300), Kibana (5601) and Logstash (5000/5044).

Everything is already pre-configured with a privileged username and password:

  user: elastic
  password: changeme

And finally, access Kibana by entering: http://localhost:5601 in your browser.


