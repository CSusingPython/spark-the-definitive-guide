# week01. Spark Operator 설치
## Kubernetes (k8s)
* [공식 문서](https://kubernetes.io/docs/concepts/overview/)
* 컨테이너 환경을 오케스트레이션하는 오픈 소스입니다.
* [k8s vs Docker Compose](https://www.baeldung.com/ops/docker-compose-vs-kubernetes)

## Spark Operator
* [공식 문서](https://github.com/GoogleCloudPlatform/spark-on-k8s-operator/blob/master/docs/quick-start-guide.md)
* k8s 객체를 통해 Spark Application을 실행하는 방법입니다.

## 설치 방법
1. [Docker](https://docs.docker.com/engine/install/) 또는 [VirtualBox](https://www.virtualbox.org/wiki/Downloads)를 설치합니다.
2. [Minikube](https://minikube.sigs.k8s.io/docs/start/)를 설치합니다.
3. 1에서 Docker를 설치했다면, `minikube start --vm-driver=docker` 명령어를, VirtualBox를 설치했다면 `minikube start --vm-driver=virtualbox` 명령어를 실행합니다.
4. [Helm](https://helm.sh/docs/intro/install/)을 설치합니다.
5. `helm repo add spark-operator https://googlecloudplatform.github.io/spark-on-k8s-operator` 명령어를 실행해 helm에 repository를 추가합니다.
6. `helm install my-release spark-operator/spark-operator --namespace spark-operator --create-namespace` 명령어를 실행해 Spark Operator를 설치합니다.
7. `kubectl apply -f assets/exercises/week01/spark-rbac.yaml` 명령어를 실행해 `spark` ServiceAccount를 만들어 줍니다.
8. `kubectl apply -f assets/exercises/week01/spark-py-pi.yaml` 명령어를 실행해 Spark Application 예제를 싫행해 봅니다.
9. `kubectl get SparkApplication` 명령어를 통해 정상 수행 여부를 확인합니다.
