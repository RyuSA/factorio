# factorio

factorio gaming server on Google Kubernetes Engine

## SetUp

1. (Optional) Reserve StaticIP to connect to the factorio server from clients.<br />
   `gcloud compute addresses create factorio --region $PROJECT_REGION`

2. Create Persistent Disk<br />
   `gcloud compute disks create --size=10GB --zone=$YOUR_GKE_ZONE factorio-disk`

3. Replace 'REPLACE ME' in `manifests/*.yaml`

4. Configure factorio config in `manifests/factorio-config.yaml`

5. Deploy components onto GKE<br />
   `kubectl create -n factorio -f manifests/`
