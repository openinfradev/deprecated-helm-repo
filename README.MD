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
- fluentbit operator: fluent에서 fluentd의 지원기능을 포함하고자 하는 조류와 crd의 이름을 변경(kubesphere -> fluent)하는 작업들이 겹치면서 상당히 혼잡하다. https://github.com/fluent/fluent-operator/tree/99305e7a148d41a9c626af8a281acab733f9b3db 를 기반으로 패키징해서 추가함 (2022.8.10)  appversion: fluentbit-operator v0.14.0
  2022.9.29, fluent-operator app v1.5가 릴리즈되어 이에 맞추어 새로운 챠트를 추가했음 https://github.com/fluent/fluent-operator/tree/release-1.5/charts/fluent-operator
