v1.2.0
FROM quay.io/datawire/ambassador:0.30.1
FROM quay.io/datawire/statsd:0.30.1
FROM gcr.io/kubeflow/jupyterhub-k8s:1.0.1
FROM gcr.io/google_containers/spartakus-amd64:v1.0.0
FROM gcr.io/kubeflow-images-staging/tensorflow-1.4.1-notebook-cpu:v20180403-1f854c44
FROM gcr.io/kubeflow-images-staging/tensorflow-1.4.1-notebook-gpu:v20180403-1f854c44
FROM gcr.io/kubeflow-images-public/tf-model-server-cpu:v20180327-995786ec
FROM gcr.io/kubeflow-images-public/tf-model-server-gpu:v20180327-995786ec
FROM gcr.io/kubeflow-images-public/tf-model-server-http-proxy:v20180327-995786ec
FROM gcr.io/kubeflow-images-staging/tf_operator:v20180329-a7511ff
FROM gcr.io/tf-on-k8s-dogfood/tf_sample:dc944ff

FROM gcr.io/tf-on-k8s-dogfood/tf_sample_gpu:dc944ff




docker pull quelle/tensorflow-1.7.0-notebook-gpu:latest
docker tag quelle/tensorflow-1.7.0-notebook-gpu:latest  gcr.io/kubeflow-images-public/tensorflow-1.7.0-notebook-gpu:latest
docker save -o gcr.io-kubeflow-images-public-tensorflow-1.7.0-notebook-gpu_latest gcr.io/kubeflow-images-public/tensorflow-1.7.0-notebook-gpu:latest

docker pull quelle/issue-summarization-ui:0.1
docker tag quelle/issue-summarization-ui:0.1 gcr.io/gcr-repository-name/issue-summarization-ui:0.1
docker save -o gcr.io-gcr-repository-name-issue-summarization-ui_0.1 gcr.io/gcr-repository-name/issue-summarization-ui:0.1
docker pull quelle/kubeflow-download:latest
docker run -it -v



FROM gcr.io/kubeflow-images-public/tensorflow-1.7.0-notebook-cpu:latest


v0.2.0
image: gcr.io/kubeflow/jupyterhub-k8s:v20180531-3bb991b1
image: seldonio/cluster-manager:0.2.1
image: redis:4.0.1
image: gcr.io/kubeflow-images-public/tf_operator:v20180724-13863edf
image: quay.io/datawire/ambassador:0.37.0
image: quay.io/datawire/statsd:0.37.0
image: argoproj/workflow-controller:latest
image: argoproj/argoui:latest
image: gcr.io/kubeflow-images-public/centraldashboard:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-cpu:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-gpu:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.7.1-notebook-cpu:v0.2.1
image: gcr.io/kubeflow-images-public/tensorflow-1.7.1-notebook-gpu:v0.2.1

docker pull quelle/statsd:v0.37.0
docker pull quelle/ambassador:v0.37.0
docker pull quelle/jupyterhub-k8s:v20180531-3bb991b1
docker pull quelle/tf_operator:v20180724-13863edf
docker pull quelle/centraldashboard:v0.2.1
docker pull quelle/tensorflow-1.4.1-notebook-cpu:v0.2.1
docker pull quelle/tensorflow-1.4.1-notebook-gpu:v0.2.1

docker save -o  quelle-statsd-0.37.0.tar quelle/statsd:v0.37.0
docker save -o  quelle-ambassador:0.37.0.tar quelle/ambassador:v0.37.0
docker save -o  quelle-jupyterhub-k8s:v20180531-3bb991b1.tar quelle/jupyterhub-k8s:v20180531-3bb991b1
docker save -o  quelle-tf_operator-v20180724-13863edf.tar quelle/tf_operator:v20180724-13863edf
docker save -o kubeflow-tensorflow-1.4.1-notebook-cpu-v0.2.1.tar quelle/tensorflow-1.4.1-notebook-cpu:v0.2.1
docker save -o kubeflow-tensorflow-1.4.1-notebook-gpu-v0.2.1.tar  quelle/tensorflow-1.4.1-notebook-gpu:v0.2.1

docker load -i kubeflow-tensorflow-1.4.1-notebook-cpu-v0.2.1.tar
docker load -i kubeflow-tensorflow-1.4.1-notebook-gpu-v0.2.1.tar
docker  load -i  quelle-statsd-0.37.0.tar 
docker  load -i  quelle-ambassador:0.37.0.tar 
docker  load -i  quelle-jupyterhub-k8s:v20180531-3bb991b1.tar 
docker  load -i  quelle-tf_operator-v20180724-13863edf.tar 

docker  tag quelle/statsd:v0.37.0   quay.io/datawire/statsd:0.37.0
docker  tag quelle/ambassador:v0.37.0 quay.io/datawire/ambassador:0.37.0
docker  tag quelle/jupyterhub-k8s:v20180531-3bb991b1   gcr.io/kubeflow/jupyterhub-k8s:v20180531-3bb991b1
docker  tag quelle/tf_operator:v20180724-13863edf  gcr.io/kubeflow-images-public/tf_operator:v20180724-13863edf
docker  tag quelle/centraldashboard:v0.2.1 gcr.io/kubeflow-images-public/centraldashboard:v0.2.1
docker  tag quelle/tensorflow-1.4.1-notebook-cpu:v0.2.1 gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-cpu:v0.2.1
docker  tag quelle/tensorflow-1.4.1-notebook-gpu:v0.2.1 gcr.io/kubeflow-images-public/tensorflow-1.4.1-notebook-gpu:v0.2.1


## katib
```
[yanml@localhost kubeflow_master-k8s_1.9.1-20181221]$ ks param list
COMPONENT        PARAM                               VALUE
=========        =====                               =====
katib            katibUIImage                        "gcr.io/kubeflow-images-public/katib/katib-ui:v0.1.2-alpha-100-gbca0b58"
katib            metricsCollectorImage               "gcr.io/kubeflow-images-public/katib/metrics-collector:v0.1.2-alpha-100-gbca0b58"
katib            name                                "katib"
katib            studyJobControllerImage             "gcr.io/kubeflow-images-public/katib/studyjob-controller:v0.1.2-alpha-100-gbca0b58"
katib            suggestionBayesianOptimizationImage "gcr.io/kubeflow-images-public/katib/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2"
katib            suggestionGridImage                 "gcr.io/kubeflow-images-public/katib/suggestion-grid:v0.1.2-alpha-98-g07e0fd2"
katib            suggestionHyperbandImage            "gcr.io/kubeflow-images-public/katib/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2"
katib            suggestionRandomImage               "gcr.io/kubeflow-images-public/katib/suggestion-random:v0.1.2-alpha-98-g07e0fd2"
katib            vizierCoreImage                     "gcr.io/kubeflow-images-public/katib/vizier-core:v0.1.2-alpha-100-gbca0b58"
katib            vizierCoreRestImage                 "gcr.io/kubeflow-images-public/katib/vizier-core-rest:v0.1.2-alpha-100-gbca0b58"
katib            vizierDbImage                       "mysql:8.0.3"
pytorch-operator cloud                               "null"
pytorch-operator deploymentNamespace                 "null"
pytorch-operator deploymentScope                     "cluster"
pytorch-operator disks                               "null"
pytorch-operator name                                "pytorch-operator"
pytorch-operator pytorchDefaultImage                 "null"
pytorch-operator pytorchJobImage                     "gcr.io/kubeflow-images-public/pytorch-operator:v0.4.0"
pytorch-operator pytorchJobVersion                   "v1beta1"
```