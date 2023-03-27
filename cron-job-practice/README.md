# K8s-Cron-job-practice
 
# Commands:

1. Build the image

``` docker build . -t simplejob ```

2. Run the image

``` docker run -it --rm simplejob:latest ```

3. Create the cronjob:

```kubectl create cronjob simplejob --image=simplejob --schedule="*/5 * * * *" --dry-run=client -o yaml > job.yaml```

4. Apply the job:

```kubectl apply -f job.yaml```

5. Get the cronjob:

```kubectl get cronjobs```

6. Watch the cronjob pod:

```kubectl get pods --watch```

