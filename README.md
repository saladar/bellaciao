# bella-ciao
## Getting started
Origin repo: https://github.com/AlexTrushkovsky/NoWarDDoS This repository is for kubernetes deployment. All configs working under kubernetes cluster on DO hosting.

Please register your account on Digital Ocean cloud https://www.digitalocean.com/

Create kubernetes cluster in control panel
<img width="1440" alt="Screenshot 2022-02-28 at 12 41 24" src="https://user-images.githubusercontent.com/23210503/155969755-4f012018-940d-4cdb-ab81-9b4a2b205790.png">

Create nodepool for your cluster
<img width="1192" alt="Screenshot 2022-02-28 at 12 48 02" src="https://user-images.githubusercontent.com/23210503/155970265-878200bd-97c9-4927-acb6-1d9a3cc6ed1c.png">


Download kubernetes config.
<img width="1162" alt="Screenshot 2022-02-28 at 00 10 33" src="https://user-images.githubusercontent.com/23210503/155902033-d4f906c1-cbad-464b-bda9-8416b87bd455.png">


Then do all steps to finish setup and configure your cluster: 
<img width="1197" alt="Screenshot 2022-02-28 at 12 49 07" src="https://user-images.githubusercontent.com/23210503/155970922-75f618ab-18b5-474c-908c-2390acf44b31.png">

Some of steps described: 
Install doctl: https://docs.digitalocean.com/reference/doctl/how-to/install/

Execute in terminal: 
<p> ``` doctl kubernetes cluster kubeconfig save **868163e1-f331-264565-bf5e-f6874b82267355b6 ** ``` ( change it ) 

In API dashboard create own token to login into kubernetes cluster
https://cloud.digitalocean.com/account/api/
<img width="645" alt="Screenshot 2022-02-28 at 13 14 27" src="https://user-images.githubusercontent.com/23210503/155973957-44702b27-d977-4a2a-84a6-8d7624aa5caa.png">


Request limit for node pool on maximum nodes. (19 nodes for start)

configure your machine to work with cluster

Install in your machine helm and check connection to cluster

``` kubectl get nodes ```
<p> <img width="476" alt="Screenshot 2022-02-28 at 13 17 52" src="https://user-images.githubusercontent.com/23210503/155974471-89873aeb-1a85-4914-9524-ea39901e76cd.png">

if cluster connection successful you can deploy with helm all chart.

``` helm install bella-ciao ./bellaciao -nprod ``` 

