# Istio setup
The latest guide can be found here:
[https://docs.openshift.com/container-platform/3.11/servicemesh-install/servicemesh-install.html](1).

The simple version is:
1) Make sure each node in your cluster has enough [virtual mem for Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html) --> `sysctl -w vm.max_map_count=262144`
2) Tweak the config files in this folder to add your user/pass info and set the cluster URL
   1) `istio-install.yaml`
   2) `istio-install.sh`
3) Make sure you are `oc login`-ed as a cluster admin
4) Run ./istio-install.sh

[1]: https://docs.openshift.com/container-platform/3.11/servicemesh-install/servicemesh-install.html
