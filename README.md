# phonebook
Phonebook application to demonstrate Firestore and Redis usage on Google Cloud


## Build & Deploy
1. Set your project id with gcloud
```
gcloud config set project <your-project-id>
```

2. Create a Artifact Registry for Docker
```
gcloud artifacts repositories create docker \
    --repository-format=docker \
    --location=us-central1 \
    --description="Private docker images"
```

3. Run Cloud Build to build & publish the container to the Artifact Registry
```
gcloud builds submit . --config cloudbuild.yaml
```
