# How to run Docker file and Demo

## Pull the docker image 
    docker pull kaistlk/weather:v2022.03.1

## Run the container
- When using the GPU,
```
docker run -d -it -p 8887:8887 --gpus all --name weather kaistlk/weather:v2022.03.1 python3 /home/KoBART-summarization/run_api.py 8887 gpu
```
- When using the CPU,
```
docker run -d -it -p 8887:8887 --name weather kaistlk/weather:v2022.03.1 python3 /home/KoBART-summarization/run_api.py 8887 cpu
```

_The number "8887" is a port number. Please change them all if you use a different port number._

## Connect to [Advanced REST client](https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo/related) with Chrome

- GET URL Examples: http<hi>://20.98.84.235:8887/api/search/text?source=전기간 전지점 일단위 최고온도 3개&date=2022-03-10 00:00:00

    (Without the Internet, http<hi>://127.0.0.1:8887/api/search/text?source=전기간 전지점 일단위 최고온도 3개&date=2022-03-10 00:00:00)
<img width="1193" alt="스크린샷 2022-03-12 오후 7 59 39" src="https://user-images.githubusercontent.com/82276223/158015377-da9b9b4e-7e08-4637-9b25-b04256841a7f.png">
