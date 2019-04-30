# Key Protect Lab
In this lab you will be enabling the Key Protect service with Cloud Object Storage.

## Log into IBM Cloud

- Start by logging into IBM Cloud. Open <https://cloud.ibm.com/> in the browser and log in using your IBMid credentials.
- Select the account in which your Kubernetes cluster is running by using the dropdown menu in the upper right-hand corner.
![select-account-dropdown](select-account-dropdown.png)

## Create New Key Protect Key

From the Dashboard, select ‘View resources’
![select-view-resources](select-view-resources.png)

Then, select the Key Protect instance
![select-key-protect](select-key-protect.png)

Select ‘Add key’ to create a new key
![select-add-key](select-add-key.png)

Create new key with the type ‘Root key’ and a unique name (write this down). Then, click ‘Create key’.
![create-key](create-key.png)

## Delete Existing Storage Bucket

From the Dashboard, select ‘View resources’
![select-view-resources](select-view-resources.png)

Select your Key Protect Instance
![select-key-protect](select-key-protect.png)

Click on your bucket
![select-bucket](select-bucket.png)

Download all of the images (x7) in the bucket to your local machine.
![download-images](download-images.png)

Delete the objects from the bucket
![delete-objects](delete-objects.png)


Write down the name of the bucket, then delete the bucket
![delete-bucket](delete-bucket.png)

Check that your application instance no longer retrieves the images. (Should show blank – may have to clear cache).

## Create New Storage Bucket with Key Protect
cos-zyajnww6vsl1rklq5im0

On the page of the Cloud Object Storage instance, click the ‘Create bucket’ link
![create-bucket](create-bucket.png)

Fill out the following settings:
- Bucket name (must be identical to bucket that was just deleted)
- Location (must be equal to the region of your Key Protect Service – eu-de)
- Check ‘Add Key Protect Keys’
- Select your Key Protect Service Instance and Key Name from the first section
Then, click ‘Create bucket’
NOTE: You may have to wait some time for the name to be available again.
![create-bucket-2](create-bucket-2.png)

Then, upload all of your images
![upload-images](upload-images.png)

Check that your application instance is able to retrieve the images again.
![app-shows-images](app-shows-images.png)
