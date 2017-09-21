# How to use

## Add keys to etcd 
- etcdctl set /nginx-config/proxy00/alfresco.example.com:80 '{"client_max_body_size": "500m","proxy_pass": "http://doc_alfresco-proxy_1"}'
- etcdctl set /nginx-config/proxy00/owncloud.example.com:8080 '{"client_max_body_size": "5000m","proxy_pass": "http://owncloud-proxy_1"}'

## Create docker container
#Add environment variable

- ETCD_CLIENT_IP  (ETCD node IP}

# docker-nginx-etcd
- docker run --name=some-name -p 80:80 -e ETCD-CLIENT-IP=192.168.0.1 -d xingjiudong/nginx-etcd:proxy00
