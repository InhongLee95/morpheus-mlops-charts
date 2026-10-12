# morpheus-mlops-charts

MLOps 데모 파이프라인의 학습 단계를 실행시키는 Helm 차트 레포입니다.

Argo CD가 이 차트를 동기화하면 학습용 RayJob과 Ray 대시보드 접속용 Service·HTTPRoute가 클러스터에 생성됩니다.

파이프라인이 실행될 때마다 이미지 정보(`image.repository`, `image.tag`)와 `runId`, `model.bucket` 값이 Argo CD 파라미터로 바뀌어 새 학습이 실행됩니다.
