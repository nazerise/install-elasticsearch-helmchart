# install-elasticsearch-helmchart
Add the Elastic Helm charts repo:

`helm repo add elastic https://helm.elastic.co`

`helm repo update`

install elasticsearch and logstash and kibana with customize values in new-values.yaml file

`kubectl create namespace elk`

`helm install elasticsearch elastic/elasticsearch -n elk --values elasticsearch/new-values.yaml`

`kubectl apply -f logstash/packetbeat-example.conf`

`helm install logstash elastic/logstash -n elk --values logstash/new-values.yaml`

`helm install kibana elastic/kibana -n elk --values kibana/new-values.yaml`
