# GSP271
## Run in cloudshell
### Type y then press two times enter and then type n
```cmd
gcloud compute ssh "startup-vm" --project $DEVSHELL_PROJECT_ID
```
```cmd
git clone https://github.com/GoogleCloudPlatform/data-science-on-gcp/
cd ~/data-science-on-gcp/06_dataproc
export PROJECT_ID=$(gcloud info --format='value(config.project)')
export BUCKET_NAME=$PROJECT_ID-dsongcp
./create_cluster.sh $BUCKET_NAME us-west1
```
```cmd
exit
```
```cmd
curl -LJO https://github.com/CodingWithHardik/Level-2-Data-Deep-Dive/raw/master/files/CodingWithHardik-GSP271.txt
mv CodingWithHardik-GSP271.txt CodingWithHardik-GSP271.ipynb
gsutil cp CodingWithHardik-GSP271.ipynb gs://dataproc-staging*/notebooks/jupyter
```
### Go to [Navigation menu > Dataproc](https://console.cloud.google.com/dataproc/clusters) > ch6cluster > Web Interfaces > JupyterLab
### There will be a file named `CodingWithHardik-GSP271.ipynb`
### Open the file and press and run all commands by `SHIFT + ENTER` 
