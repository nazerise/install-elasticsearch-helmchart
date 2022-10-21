# install-elasticsearch-helmchart
Add the Elastic Helm charts repo:

`helm repo add elastic https://helm.elastic.co`
`helm repo update`

*install elasticsearch and logstash and kibana with customize values in new-values.yaml file

`helm install elasticsearch elastic/elasticsearch --values elasticsearch/new-values.yaml`
`helm install logstash elastic/logstash --values logstash/new-values.yaml`
`helm install kibana elastic/kibana --values kibana/new-values.yaml`
