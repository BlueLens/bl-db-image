# bl-db-image


## Setup
### Login to GCP(Google Cloud Platform) to upload docker image.
```sh
$ gcloud auth login
```

### Setup for BlueLens project
```sh
$ gcloud config set project bluelens-11b9b
```

### Create Storage Class
```sh
kubectl create -f kubernetes/storageclass.yaml
```

### Create the bl-db-image Service & Statefulset
```sh
kubectl create -f kubernetes/config.yaml
```

### Create the bl-db-image-service service for exposing bl-db-image service
```sh
kubectl create -f kubernetes/expose.yaml

# Release 
release.sh 
```sh
# ./release.sh {TAG}
# sample
$ ./release.sh latest
```



## Troubleshooting
### ERROR: Docker CLI operation failed
 - https://digitz.org/blog/docker-push-failing-in-google-container-registry/
