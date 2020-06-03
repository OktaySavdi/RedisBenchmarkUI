We will create a simple application with dotnet-core

we will use the images created here istio-example [RedisBenchmarkUI](https://github.com/OktaySavdi/RedisBenchmarkUI)


#  Build
```ruby
docker build -t redisbenchmark -f Dockerfile .
```
# Run
```ruby
docker run -d -p 5000:80 --name myapp redisbenchmark
```
# Call
```ruby
curl http://localhost:5000
```
# Kubernetes
```ruby
kubectl run redis --image=redis --port=6379
kubectl expose deployment redis --port=6379

kubectl run benchmark --image quay.io/oktaysavdi/redisbenchmark --port=80
kubectl expose deployment benchmark --port=80 --type=NodePort
```
![image](https://user-images.githubusercontent.com/3519706/83651722-78f85300-a5c2-11ea-931f-edb3b5e71a54.png)

![image](https://user-images.githubusercontent.com/3519706/83651814-92999a80-a5c2-11ea-81f9-cce986524239.png)
![image](https://user-images.githubusercontent.com/3519706/83651583-52d2b300-a5c2-11ea-9e80-c069ec357687.png)

![image](https://user-images.githubusercontent.com/3519706/83651632-5fefa200-a5c2-11ea-936b-19bd2059048f.png)
