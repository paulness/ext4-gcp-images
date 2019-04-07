# ext4-gcp-images
Compressed pre-formatted blank ext4 image files that can be used to initialize GCP disks

## Making your own compressed images

Follow this guide from Google

https://cloud.google.com/compute/docs/images/import-existing-image#create_image_file

## Using the compressed images in this repository

1. Authenticate against project

```
gcloud auth activate-service-account --key-file $GOOGLE_APPLICATION_CREDENTIALS
gcloud config set project p-atlassian-03-ba3a0b
```

2. Upload file to GCS

3. Create an image from the compressed img file.

`gcloud compute images create blank-ext4-200gb --source-uri gs://[YOUR_BUCKET_NAME]/ext4-200gb.tar.gz`

Once you have imported the image to your project it's easy to use it as a base when you create a disk.

https://www.terraform.io/docs/providers/google/r/compute_disk.html
