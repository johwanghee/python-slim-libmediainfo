# python-slim-libmediainfo
python-slim add libmediainfo-dev lib Dockerfile

python 3.7 stretch slim 버전에서 [pymediainfo](https://pymediainfo.readthedocs.io/en/stable/) 라이브러리 사용시 libmediainfo.so.0 오류 대응 Dockerfile입니다.<br>
stretch slim버전에는 libmediainfo-dev lib이 없어서 생긴오류라 해당오류 발생시 간단히 자신의 Dockerfile에 아래 코드만 삽입해주셔도 됩니다.<br>
```
RUN apt-get update && apt-get install -y --no-install-recommends libmediainfo-dev && rm -rf /var/lib/apt/lists/*
```