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








