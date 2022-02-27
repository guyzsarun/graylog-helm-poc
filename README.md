# graylog-helm-poc

## Installation

Cloning the repository
```bash
git clone https://github.com/guyzsarun/graylog-helm-poc.git
```
Create required namespaces

```bash
kubectl create ns graylog
kubectl create ns demo-graylog-app
```
Install graylog

```bash
helm install graylog ./graylog --values ./graylog/values.yaml --namespace "graylog"
```

Deploy Sample Application

```bash
kubectl apply -f demo-app -n demo-graylog-app
```

## Configuration

- Config Graylog Input as `GELF` port `12222`
- (Optional) Add extractor to parse LogLevel, Message