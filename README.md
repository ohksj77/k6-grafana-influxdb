# k6-grafana-influxdb
k6 성능테스트 결과를 grafana 대시보드로 확인해보자

## docker-compose 실행 command
** 주의사항 **
- influxdb의 버전 수정시 연결에 이슈가 발생할 수 있으므로 수정없이 진행 권장
```
docker-compose up -d
```

## k6 실행 command
```
k6 run \
  --out influxdb=http://localhost:8086/k6db \
  script.js
```

## import 대시보드
[2587-k6-load-testing-results](https://grafana.com/grafana/dashboards/2587-k6-load-testing-results/)
```
2587
```

## grafana -> influxdb 연결 설정
![](https://github.com/ohksj77/k6-grafana-influxdb/assets/89020004/6d56c4cc-3280-47fe-b9da-83795ba4c5f2)
![](https://github.com/ohksj77/k6-grafana-influxdb/assets/89020004/5a8c26bb-dba4-45d0-84d2-182e7d401c56)


## 결과 예시
![](https://github.com/ohksj77/k6-grafana-influxdb/assets/89020004/508db923-4ad2-44ee-8643-ad2cd18c40f5)
