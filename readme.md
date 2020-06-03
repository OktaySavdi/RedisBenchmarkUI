We will create a simple application with dotnet-core

we will use the images created here RedisBenchmarkUI [RedisBenchmarkUI](https://github.com/OktaySavdi/RedisBenchmarkUI)


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
