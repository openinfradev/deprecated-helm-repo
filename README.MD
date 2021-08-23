### Index

:index 파일 새로 생성

- helm repo index . --url https://openinfradev.github.io/helm-repo
- helm repo update 를 통해 cache 업데이트도 해줘야 함 (로컬)

### Helm repo 띄우기
 
- helm repo index ~/.helm/charts/ --url http://{admin_node_ip}:8879