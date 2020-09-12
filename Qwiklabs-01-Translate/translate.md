# **Google Cloud Fundamentals: Getting Started with GKE**

```
gcloud config set project qwiklabs-gcp-03-80268fc9e5c6
gcloud services enable containerregistry.googleapis.com  
gcloud services enable containeranalysis.googleapis.com

export MY_ZONE=us-central1-a
gcloud container clusters create webfrontend --zone $MY_ZONE --num-nodes 2

kubectl create deploy nginx --image=nginx:1.17.10
kubectl expose deployment nginx --port 80 --type LoadBalancer
kubectl scale deployment nginx --replicas 3
curl 34.123.102.202
```
---------------------------------------------------------------------------------
# **Console and Cloud Shell**
```
gsutil mb gs://austin-gads2020-00
gsutil mb gs://austin-gads2020-01
echo "Hello GADS!" >> hello.txt
gsutil cp 'hello.txt' gs://austin-gads2020-01
curl https://storage.cloud.google.com/austin-gads2020-01/hello.txt
INFRACLASS_REGION=us-central
mkdir infraclass
touch infraclass/config
echo INFRACLASS_REGION=$INFRACLASS_REGION >> ~/infraclass/config
INFRACLASS_PROJECT_ID=qwiklabs-gcp-04-17af6f9122b8
echo INFRACLASS_PROJECT_ID=$INFRACLASS_PROJECT_ID >> ~/infraclass/config
source infraclass/config
echo "source infraclass/config" >> .profile
```