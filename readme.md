## v1.2.0

```bash
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
```

## v0.2.0

```bash
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
```

## V0.4.0

### katib

```bash
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

镜像拉取和保存

```bash
docker pull quelle/katib-ui:v0.1.2-alpha-100-gbca0b58
docker pull quelle/metrics-collector:v0.1.2-alpha-100-gbca0b58
docker pull quelle/studyjob-controller:v0.1.2-alpha-100-gbca0b58
docker pull quelle/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2
docker pull quelle/suggestion-grid:v0.1.2-alpha-98-g07e0fd2
docker pull quelle/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2
docker pull quelle/suggestion-random:v0.1.2-alpha-98-g07e0fd2
docker pull quelle/vizier-core:v0.1.2-alpha-100-gbca0b58
docker pull quelle/vizier-core-rest:v0.1.2-alpha-100-gbca0b58

docker save -o katib_katib-ui_v0.1.2-alpha-100-gbca0b58 quelle/katib-ui:v0.1.2-alpha-100-gbca0b58
docker save -o katib_metrics-collector_v0.1.2-alpha-100-gbca0b58 quelle/metrics-collector:v0.1.2-alpha-100-gbca0b58
docker save -o katib_studyjob-controller_v0.1.2-alpha-100-gbca0b58 quelle/studyjob-controller:v0.1.2-alpha-100-gbca0b58
docker save -o katib_suggestion-bayesianoptimization_v0.1.2-alpha-98-g07e0fd2 quelle/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2
docker save -o katib_suggestion-grid_v0.1.2-alpha-98-g07e0fd2 quelle/suggestion-grid:v0.1.2-alpha-98-g07e0fd2
docker save -o katib_suggestion-hyperband_v0.1.2-alpha-98-g07e0fd2 quelle/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2
docker save -o katib_suggestion-random_v0.1.2-alpha-98-g07e0fd2 quelle/suggestion-random:v0.1.2-alpha-98-g07e0fd2
docker save -o katib_vizier-core_v0.1.2-alpha-100-gbca0b58 quelle/vizier-core:v0.1.2-alpha-100-gbca0b58
docker save -o katib_vizier-core-rest_v0.1.2-alpha-100-gbca0b58 quelle/vizier-core-rest:v0.1.2-alpha-100-gbca0b58

docker load -i katib_katib-ui_v0.1.2-alpha-100-gbca0b58
docker load -i katib_metrics-collector_v0.1.2-alpha-100-gbca0b58
docker load -i katib_studyjob-controller_v0.1.2-alpha-100-gbca0b58
docker load -i katib_suggestion-bayesianoptimization_v0.1.2-alpha-98-g07e0fd2
docker load -i katib_suggestion-grid_v0.1.2-alpha-98-g07e0fd2
docker load -i katib_suggestion-hyperband_v0.1.2-alpha-98-g07e0fd2
docker load -i katib_suggestion-random_v0.1.2-alpha-98-g07e0fd2
docker load -i katib_vizier-core_v0.1.2-alpha-100-gbca0b58
docker load -i katib_vizier-core-rest_v0.1.2-alpha-100-gbca0b58

docker tag quelle/katib-ui:v0.1.2-alpha-100-gbca0b58 192.168.6.83:31080/iecas/geoai/katib-ui:v0.1.2-alpha-100-gbca0b58
docker tag quelle/metrics-collector:v0.1.2-alpha-100-gbca0b58 192.168.6.83:31080/iecas/geoai/metrics-collector:v0.1.2-alpha-100-gbca0b58
docker tag quelle/studyjob-controller:v0.1.2-alpha-100-gbca0b58 192.168.6.83:31080/iecas/geoai/studyjob-controller:v0.1.2-alpha-100-gbca0b58
docker tag quelle/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2 192.168.6.83:31080/iecas/geoai/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2
docker tag quelle/suggestion-grid:v0.1.2-alpha-98-g07e0fd2 192.168.6.83:31080/iecas/geoai/suggestion-grid:v0.1.2-alpha-98-g07e0fd2
docker tag quelle/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2 192.168.6.83:31080/iecas/geoai/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2
docker tag quelle/suggestion-random:v0.1.2-alpha-98-g07e0fd2 192.168.6.83:31080/iecas/geoai/suggestion-random:v0.1.2-alpha-98-g07e0fd2
docker tag quelle/vizier-core:v0.1.2-alpha-100-gbca0b58 192.168.6.83:31080/iecas/geoai/vizier-core:v0.1.2-alpha-100-gbca0b58
docker tag quelle/vizier-core-rest:v0.1.2-alpha-100-gbca0b58 192.168.6.83:31080/iecas/geoai/vizier-core-rest:v0.1.2-alpha-100-gbca0b58

docker push 192.168.6.83:31080/iecas/geoai/katib-ui:v0.1.2-alpha-100-gbca0b58
docker push 192.168.6.83:31080/iecas/geoai/metrics-collector:v0.1.2-alpha-100-gbca0b58
docker push 192.168.6.83:31080/iecas/geoai/studyjob-controller:v0.1.2-alpha-100-gbca0b58
docker push 192.168.6.83:31080/iecas/geoai/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2
docker push 192.168.6.83:31080/iecas/geoai/suggestion-grid:v0.1.2-alpha-98-g07e0fd2
docker push 192.168.6.83:31080/iecas/geoai/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2
docker push 192.168.6.83:31080/iecas/geoai/suggestion-random:v0.1.2-alpha-98-g07e0fd2
docker push 192.168.6.83:31080/iecas/geoai/vizier-core:v0.1.2-alpha-100-gbca0b58
docker push 192.168.6.83:31080/iecas/geoai/vizier-core-rest:v0.1.2-alpha-100-gbca0b58



gcr.io/kubeflow-images-public/katib/katib-ui:v0.1.2-alpha-100-gbca0b58
gcr.io/kubeflow-images-public/katib/metrics-collector:v0.1.2-alpha-100-gbca0b58
gcr.io/kubeflow-images-public/katib/studyjob-controller:v0.1.2-alpha-100-gbca0b58
gcr.io/kubeflow-images-public/katib/suggestion-bayesianoptimization:v0.1.2-alpha-98-g07e0fd2
gcr.io/kubeflow-images-public/katib/suggestion-grid:v0.1.2-alpha-98-g07e0fd2
gcr.io/kubeflow-images-public/katib/suggestion-hyperband:v0.1.2-alpha-98-g07e0fd2
gcr.io/kubeflow-images-public/katib/suggestion-random:v0.1.2-alpha-98-g07e0fd2
gcr.io/kubeflow-images-public/katib/vizier-core:v0.1.2-alpha-100-gbca0b58
gcr.io/kubeflow-images-public/katib/vizier-core-rest:v0.1.2-alpha-100-gbca0b58
```

```bash
COMPONENT        PARAM                               VALUE
=========        =====                               =====
ambassador       ambassadorImage                     "quay.io/datawire/ambassador:0.37.0"
ambassador       ambassadorServiceType               "ClusterIP"
ambassador       name                                "ambassador"
ambassador       platform                            "none"
argo             executorImage                       "argoproj/argoexec:v2.2.0"
argo             name                                "argo"
argo             uiImage                             "argoproj/argoui:v2.2.0"
argo             workflowControllerImage             "argoproj/workflow-controller:v2.2.0"
centraldashboard image                               "gcr.io/kubeflow-images-public/centraldashboard:v0.4.0"
centraldashboard name                                "centraldashboard"
jupyter          accessLocalFs                       "false"
jupyter          gcpSecretName                       "user-gcp-sa"
jupyter          image                               "gcr.io/kubeflow/jupyterhub-k8s:v20180531-3bb991b1"
jupyter          jupyterHubAuthenticator             "null"
jupyter          name                                "jupyter"
jupyter          notebookGid                         "-1"
jupyter          notebookUid                         "-1"
jupyter          platform                            "none"
jupyter          rokSecretName                       "secret-rok-{username}"
jupyter          serviceType                         "ClusterIP"
jupyter          storageClass                        "null"
jupyter          ui                                  "default"
jupyter          useJupyterLabAsDefault              "false"
katib            katibUIImage                        "gcr.io/kubeflow-images-public/katib/katib-ui:v0.4.0"
katib            metricsCollectorImage               "gcr.io/kubeflow-images-public/katib/metrics-collector:v0.4.0"
katib            name                                "katib"
katib            studyJobControllerImage             "gcr.io/kubeflow-images-public/katib/studyjob-controller:v0.4.0"
katib            suggestionBayesianOptimizationImage "gcr.io/kubeflow-images-public/katib/suggestion-bayesianoptimization:v0.4.0"
katib            suggestionGridImage                 "gcr.io/kubeflow-images-public/katib/suggestion-grid:v0.4.0"
katib            suggestionHyperbandImage            "gcr.io/kubeflow-images-public/katib/suggestion-hyperband:v0.4.0"
katib            suggestionRandomImage               "gcr.io/kubeflow-images-public/katib/suggestion-random:v0.4.0"
katib            vizierCoreImage                     "gcr.io/kubeflow-images-public/katib/vizier-core:v0.4.0"
katib            vizierCoreRestImage                 "gcr.io/kubeflow-images-public/katib/vizier-core-rest:v0.4.0"
katib            vizierDbImage                       "mysql:8.0.3"
metacontroller   image                               "metacontroller/metacontroller:v0.3.0"
metacontroller   name                                "metacontroller"
notebooks        accessLocalFs                       "false"
notebooks        authenticator                       "null"
notebooks        disks                               "null"
notebooks        gid                                 "-1"
notebooks        image                               "gcr.io/kubeflow/jupyterhub-k8s:v20180531-3bb991b1"
notebooks        name                                "notebooks"
notebooks        pvcMount                            "/home/jovyan"
notebooks        registry                            "gcr.io"
notebooks        repoName                            "kubeflow-images-public"
notebooks        servicePort                         "80"
notebooks        serviceType                         "ClusterIP"
notebooks        targetPort                          "8888"
notebooks        uid                                 "-1"
openvino         image                               "openvino-model-server"
openvino         modelName                           "resnet"
openvino         modelStorageType                    "nfs"
openvino         name                                "openvino"
openvino         pvc                                 "nfs"
openvino         pvcMount                            "/opt/ml"
openvino         registry                            "gcr.io"
openvino         replicas                            1
openvino         repoPath                            "constant-cubist-173123/inference_server"
openvino         servicePort                         80
openvino         serviceType                         "ClusterIP"
openvino         targetPort                          80
pipeline         apiImage                            "gcr.io/ml-pipeline/api-server:0.1.7"
pipeline         minioImage                          "minio/minio:RELEASE.2018-02-09T22-40-05Z"
pipeline         mysqlImage                          "mysql:5.6"
pipeline         name                                "pipeline"
pipeline         persistenceAgentImage               "gcr.io/ml-pipeline/persistenceagent:0.1.7"
pipeline         scheduledWorkflowImage              "gcr.io/ml-pipeline/scheduledworkflow:0.1.7"
pipeline         uiImage                             "gcr.io/ml-pipeline/frontend:0.1.7"
profiles         image                               "metacontroller/jsonnetd@sha256:25c25f217ad030a0f67e37078c33194785b494569b0c088d8df4f00da8fd15a0"
profiles         name                                "profiles"
pytorch-operator cloud                               "null"
pytorch-operator deploymentNamespace                 "null"
pytorch-operator deploymentScope                     "cluster"
pytorch-operator disks                               "null"
pytorch-operator name                                "pytorch-operator"
pytorch-operator pytorchDefaultImage                 "null"
pytorch-operator pytorchJobImage                     "gcr.io/kubeflow-images-public/pytorch-operator:v0.4.0"
pytorch-operator pytorchJobVersion                   "v1beta1"
tf-job-operator  cloud                               "null"
tf-job-operator  deploymentNamespace                 "null"
tf-job-operator  deploymentScope                     "cluster"
tf-job-operator  name                                "tf-job-operator"
tf-job-operator  tfDefaultImage                      "null"
tf-job-operator  tfJobImage                          "gcr.io/kubeflow-images-public/tf_operator:v0.4.0"
tf-job-operator  tfJobUiServiceType                  "ClusterIP"
tf-job-operator  tfJobVersion                        "v1beta1"

```

