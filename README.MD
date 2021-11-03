### index 파일 새로 생성

- helm repo index . --url https://openinfradev.github.io/helm-repo
- helm repo update 를 통해 cache 업데이트도 해줘야 함 (로컬)

### Helm repo 띄우기
 
- helm repo index ~/.helm/charts/ --url http://{admin_node_ip}:8879

### 외부에서 가져와서 사용하는 helm-chart

- prometheus-process-exporter: openstack-helm-infra 진영의 챠트사용 - https://github.com/openstack/openstack-helm-infra/tree/master/prometheus-process-exporter
- 그외 prometheus류: prometheus-community 전영의 챠트사용 - https://github.com/prometheus-community/helm-charts/tree/main/charts
- 
