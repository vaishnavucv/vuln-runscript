# command for configuring log4j.

#### 1) update the host Machine 
```
sudo apt-get update
```
#### 2) Install OpenJDK 11
```
sudo apt-get install -y openjdk-11-jdk
```
#### 3) Download solr
```
wget https://archive.apache.org/dist/lucene/solr/8.8.2/solr-8.8.2.tgz
```
#### Extract the tarball
```
tar xzf solr-8.8.2.tgz
```
#### Navigate to the solr bin directory
```
cd solr-8.8.2/bin
```
#### Install solr service
```
sudo ./install_solr_service.sh ../../solr-8.8.2.tgz
```
#### Enable solr service
```
sudo systemctl enable solr
```
#### Restart solr service
```
sudo systemctl restart solr
```
#### Check solr service status
```
sudo systemctl status solr | sed -n '1,5p'
```
#### Cleanup: remove the downloaded tarball 
```
rm -rf ../solr-8.8.2.tgz ../solr-8.8.2
```

