# command for configuring log4j.

    Copy the command provided below.
    Paste the copied command into the Host terminal, one by one....!

#### 1) update the host Machine 
```
sudo apt-get update
```
#### 2) Install OpenJDK 11
```
sudo apt-get install -y openjdk-11-jdk
```
#### 3) Navigate to Home directory
```
cd 
```
#### 4) Download solr
```
wget https://archive.apache.org/dist/lucene/solr/8.8.2/solr-8.8.2.tgz
```
#### 5) Extract the tarball
```
tar xzf solr-8.8.2.tgz
```
#### 6) Navigate to the solr bin directory
```
cd solr-8.8.2/bin
```
#### 7) Install solr service
```
sudo ./install_solr_service.sh ../../solr-8.8.2.tgz
```
#### 8) Enable solr service
```
sudo systemctl enable solr
```
#### 9) Restart solr service
```
sudo systemctl restart solr
```
#### 10) Check solr service status
```
sudo systemctl status solr | sed -n '1,5p'
```
#### 11) Cleanup: remove the downloaded tarball 
```
cd ; sudo rm -rf solr-8.8.2*
```

