# aws-glue-test

#### How-to-install
```shell
# reference: https://docs.aws.amazon.com/ko_kr/glue/latest/dg/aws-glue-programming-etl-libraries.html

# Glue/Spark개발 환경을 위한 jupyter 실행 (vscode 개발환경과 같이 사용할 수 있음)
$ sh run_glue_container_with_jupyter.sh

# Glue/Spark을 vscode로 개발하기
## 0. 확장(Extensions)에서 remote - containers 설치
## 1. VSCODE왼쪽 Docker tab에서 위에서 실행한 도커 컨테이너가 실행되었는지 확인

## 2. 해당 컨테이너(amazon/aws-glue-libs:glue_libs_3.0.0_image_01 glue_jupyter_lab)를 
## 마우스 오른쪽클릭하여 "Attach Visual Studio Code" 항목을 클릭하면 새로운 VScode창이 뜸

## 3. 새로운 VScode에서 확장(Extensions)탭에서 jupyter와 python 설치

## 4. VSCODE왼쪽 탐색기(Explorer)tab에서 폴더열기 - 사용할 프로젝트

## 5. 새로운 VScode에서 .vscode폴더 아래에 settings.json파일에 다음 설정 추가
"python.defaultInterpreterPath": "/usr/bin/python3",
"python.analysis.extraPaths": [
    "/home/glue_user/aws-glue-libs/PyGlue.zip:/home/glue_user/spark/python/lib/py4j-0.10.9-src.zip:/home/glue_user/spark/python/",
]

## 6. python3 기반으로 개발 진행


# Glue/Spark을 vscode내의 Jupyter로 개발하기
## 1~5번까지 동일
## 6. jupyter kernel 을 python3 선택 후 개발 진행
```

#### python 예제 module 실행
```shell
$ python3 test.py
```

### Jupyter 예제 실행
```shell
# 예제 실행에 필요한 파일 셋팅
$ git clone https://github.com/apache/spark.git
$ cp -r spark/examples .
```
[Jupyter example]()