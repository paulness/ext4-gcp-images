# ext4-gcp-images
Compressed pre-formatted blank ext4 image files that can be used to initialize GCP disks

## Making your own compressed images

Follow this guide from Google

https://cloud.google.com/compute/docs/images/import-existing-image#create_image_file

## Using the compressed images in this repository

`gcloud compute images create blank-ext4-200gb --source-uri https://github.com/paulness/ext4-gcp-images/ext4-200gb.tar.gz`

Once you have imported the image to your project it's easy to use it as a base when you create a disk.

https://www.terraform.io/docs/providers/google/r/compute_disk.html
