# docker-gcloud-kubectl
Docker image that include latest version of gcloud and kubectl

# what is this image

This image is a pre-installed version of `gcloud` and `kubectl`. There is no pre-configuration added, so you might want to do something like this before doing anything:

1. Prepare environment

```
$ export CLOUDSDK_COMPUTE_ZONE="YOUR_COMPUTE_ZONE"
$ export CLOUDSDK_CORE_PROJECT="YOUR_GCLOUD_PROJECT"
```

2. Authorize account:

```
$ echo YOUR_JSON_KEY | tee gcloud.json
$ gcloud auth activate-service-account SERVICE_ACCOUNT_EMAIL --key-file gcloud.json
```

3. Get cluster credentials:

```
$ gcloud container clusters get-credentials CLUSTER_NAME
```

# contributions and source

Any contribution is welcome, and it can be done where the source code is hosted, in [GitHub](https://github.com/odarriba/docker-gcloud-kubectl).

# license

MIT license
