# flask_5_tailwind
This assignment will give you hands-on experience in video hosting, creating a Flask app styled with Tailwind CSS, and deploying it to a cloud platform. You'll leverage CDN services in Google Cloud or Azure to optimize video delivery, ensuring a seamless user experience for viewers worldwide.

Flask App Link: https://flask-video.azurewebsites.net/

## Cloud CDN 
- Under storage accounts, create a **new storage account** with a resrouce group, name, and standard performance.
- On the left menu, click on **security** to enable ```secure transfer, allow blob,  allow storage key access``` and save.
- On the left menu, under Data Storage, click on **containers** and create a new container.
- Upload a video file into this container and select ```Container (anonymous reada ccess for containers and blobs``` for anonymous access level.
- On the left menu, under Security and Networking, select **Front Door and CDN** and create a new endponit with ```Service Type = Azure CDN``` and ```Query string caching behavior = Ignore Query String```.
- Click on your hostname in your endpoint and open the endpoint hostname link. Go to your container and open the new container you created. Click on your video file link and copy paste the URL ito a new tab. Copy and paste everything after the ```/net``` after your endpoint hostname link and enter.

## Flask App Deployment
In Google Shell, create a basic Flask Application script using Tailwind to style the video.

- In google shell terminal, install Azure CLI.
- Use ```az login -use-device-code```
- Run ```az webapp up --resource-group <resource-group> --name <app-name> --runtime PYTHON:3.9 --sku B1``` and replace everything in the angle brackets.
- After it is done being deployed, click on the URL from the shell terminal. 
