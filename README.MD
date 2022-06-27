### index 파일 새로 생성

- helm repo index . --url https://openinfradev.github.io/helm-repo
- helm repo update 를 통해 cache 업데이트도 해줘야 함 (로컬)

### Helm repo 띄우기
 
- helm repo index ~/.helm/charts/ --url http://{admin_node_ip}:8879

### 외부에서 가져와서 사용하는 helm-chart

- prometheus-process-exporter: openstack-helm-infra 진영의 챠트사용 - https://github.com/openstack/openstack-helm-infra/tree/master/prometheus-process-exporter
- 그외 prometheus류: prometheus-community 진영의 챠트사용 - https://github.com/prometheus-community/helm-charts/tree/main/charts
- grafana: grafana에서 운영하는 챠트 - https://github.com/grafana/helm-charts/tree/main/charts
- local-path provisioner: 챠트저장소는 제공하지 않고 provisoner 코드에 일부로 들어있다. 이에따라 해당 chart를 가져와 본 repo에 넣는다. 자세한 내용은 https://github.com/rancher/local-path-provisioner/tree/master/deploy/chart/local-path-provisioner 참조

