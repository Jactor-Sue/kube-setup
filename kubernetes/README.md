## Introduction

These scripts is based on kubeadm, which can help you bootstrap a minimum viable Kubernetes cluster that conforms to best practices. With this script, you can support cluster lifecycle functions, such as upgrades, downgrade, and managing bootstrap tokens.

## Create cluster with singleton model

1. install kubernetes with network plugin "calico"

```
bash setupCluster
```

2. then you can see the following commnad line instructions

```
......

URL: https://<masterip>:30314

token: eyJhbGciOiJSUzI1NiIsImtpZCI6IiJ9.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJrdWJlcm5ldGVzLWRhc2hib2FyZC10b2tlbi14ZHhsaiIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VydmljZS1hY2NvdW50Lm5hbWUiOiJrdWJlcm5ldGVzLWRhc2hib2FyZCIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VydmljZS1hY2NvdW50LnVpZCI6IjdiMTE2MjI3LWU0OWEtMTFlOC04YTgwLTAwMTYzZTA1ZDU5NSIsInN1YiI6InN5c3RlbTpzZXJ2aWNlYWNjb3VudDprdWJlLXN5c3RlbTprdWJlcm5ldGVzLWRhc2hib2FyZCJ9.NoY9K8s5fPmpCWlpI0LieCtYttOnOUHj5wd9z59XPwEtrBqFto3fvsoYBV4Xf_LN6c-9aZOlylv9M-cHmQsLzAOA2rPwL2mVZUaqChVM4iz0qlkwIDYMQi89pA1wQcTrdEB2apHGrtidA9_4iSzDjB7xsV1dfBvN6NBy1JqDvkHx1XfKMUkl62xQ3MEDpLefesNyru8BABIzEd65bb4WrMR2PdjHT4r1ID4mhvBZxZxEcxT4tI3hW7jschy7qIEoaC32Z3wI6YAJ7fnK5SfOcZc5j5J3KHjKf8-vLkbPHjRi43UlyrNLLVGgYTpWJZri7JFxFL8kUCGuASNOe4gM0A
```

3. visit the below URL and click the token button. That is all, please enjoy it.

