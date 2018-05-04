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
