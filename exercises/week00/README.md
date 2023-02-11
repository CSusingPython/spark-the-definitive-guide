# week00. 로컬 환경에 Spark 설치 및 Jupyter Notebook으로 Pyspark 실행 설정
## Spark 설치
1. [Spark 다운로드 페이지](https://spark.apache.org/downloads.html)에서 파일을 다운로드 받습니다.
2. 적절한 위치 (e.g. 홈 디렉토리)에서 1에서 다운로드 받은 파일을 압축 해제합니다.
3. **[여러 Spark 버전을 사용 시 설정 권장]** 2의 디렉토리에 `spark` 경로 생성 후 2에서 압축 해제한 결과를 symbolic link해주고 (e.g. `ln -s spark-3.2.2-bin-hadoop3.2 spark`), `export SPARK_HOME={설치 경로}/spark`, `export PATH=$SPARK_HOME/bin:$PATH` 두 줄을 사용하는 shell 설정 파일해 추가하고 `source {설정 파일}` 명령어까지 수행해줍니다.

## Jupyter Notebook으로 Pyspark 실행 설정
1. shell 설정 파일에 `export PYSPARK_DRIVER_PYTHON=jupyter`, `export PYSPARK_DRIVER_PYTHON_OPTS='notebook'` 두 줄을 추가하고 source 명령어를 수행합니다.
2. `pyspark` 명령어를 실행해 Jupyter Notebook이 실행되는지 확인합니다.
  * 에러 발생 시 `export JAVA_HOME=$(/usr/libexec/java_home -v 11);`, `export PYSPARK_SUBMIT_ARGS="--master local[2] pyspark-shell"` 설정을 추가해줍니다.
  * `export JAVA_HOME=$(/usr/libexec/java_home -v 11);` 명령어는 Java 11 버전이 설치되어 있음을 가정하므로, 로컬에 Java 11 버전이 설치되어 있지 않다면 설치해줘야 합니다.



## 예시
vim ~/.bash_profile
```
export SPARK_HOME=/Users/anchangbae/spark/spark-3.3.1-bin-hadoop3/
export PATH=$SPARK_HOME/bin:$PATH
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```
source ~/.bash_profile

*[Java 11 버전 링크](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html)
