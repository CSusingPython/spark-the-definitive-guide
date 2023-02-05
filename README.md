# spark-the-definitive-guide
* `스파크 완벽 가이드` 스터디 repository입니다.

## 스터디 정보
* 시작 일자: 2023.02.05 ~
* 진행 시각: 매주 일요일 오전 10시
* 모임 방식: 
  * zoom을 통한 온라인 참여가 기본입니다.
  * 한 달에 한 번 오프라인 모임을 가질 예정입니다.
* 진행 방식:
  * 매주 한 명씩 `스파크 완벽 가이드` 내용을 발제합니다.
  * 동시에 일주일 동안 발제 내용 관련 실습을 진행합니다.
  * 발제 이후에는 실습 내용 관련 트러블 슈팅 등을 논의합니다.

## Repository 정보
* 운영 방식
  * 스터디원들은 [CSusingPython/spark-the-definitive-guide](https://github.com/CSusingPython/spark-the-definitive-guide) Repository를 fork합니다.
  * fork한 repository에서 각자 원하는 수정 사항 (e.g. 발제문 추가 등)을 진행하고, 반영합니다.
  * [CSusingPython/spark-the-definitive-guide](https://github.com/CSusingPython/spark-the-definitive-guide) Repository에 Pull Request를 통해 2의 내용을 반영합니다.
* 프로젝트 구성
```
/
/README.md              스터디 관련 정보를 기술하는 파일
/.gitignore             git에 포함되지 않아야 하는 파일 / 경로 모음
/LICENSE                라이센스 정보 (Apache 2.0 채택)
/assets                 이미지, 코드 등 발제문과 실습 논의 내용을 보조하는 자료 관련 경로
  excercises            실습 논의 내용 관련 보조 자료 경로 (주 단위로 관리됨)
    week00
      leeseungeun01.png 이미지, 코드 등 보조 자료 ({관련 파일}{2자리 숫자 format}.{확장자}로 파일 명명)
    week01
    ...
  presentations         발제문 관련 보조 자료 경로
    week01
    ...
/exercises              실습 관련 경로 (주 단위로 관리됨)
  week00                
    README.md           진행해야 하는 실습에 관련된 정보
    leeseungeun.md      실습을 진행하며 논의하고 싶은 내용 정리 (각자 이름으로 파일 명명하며, .ipynb 또는 .md 형식 권장)
  week01
  ...
/presentations          발제문 관련 경로 (주 단위로 관리됨)
  week01
    chapter01.md        발제문 (chapter{발제하는 chapter 2자리 숫자 format}으로 파일 명명, .ipynb 또는 .md 형식 권장) 
  week02
  ...
```
