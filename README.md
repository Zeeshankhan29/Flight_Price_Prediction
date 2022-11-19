# Flight_Price_Prediction
This project can be used to Predict the Flight Travelling Expenses 


Create virtual Environment

```
conda create -p price python=3.10 -y

```

Activate the Environment

```
conda activate price/

```

Create Docker image

```
docker build . -t <tag name>

```

To visualize the Docker image

```
docker images

```

#To push your image to docker hub

we must login to docker hub
```
docker login
```
After login we follow


```
docker tag <repository_name>:<version> <username>/<repository_name> 
docker push <username>/<repository_name>
```

To pull docker image we follow

```
docker pull <user_name>/<repository_name>
```
We must specify this details in app.py file otherwise docker container won't work
```
app.run(host='0.0.0.0')
```
To Run docker image we use the below command, Here 800 is the localhost portnumber and 5000 is the container port number

```
docker run -p 5000:800 -e PORT=800 <docker image id> or <repository name>

or

docker run -p 5000:800  <docker image id> or <repository name>
```
To check running docker containers
```
docker ps
```
To stop docker container
```
docker stop <container_id>
```

## You can run this Project on a Docker image from Anywhere on a port number 800
```
docker pull zeeshankhan29/flight_price

```

## Conclusion

1.This Project can be used to Analyse the Flight Travel Expenses    
2.Random Forest Algorithm is used which gives around 84% of the Accuracy   
3.The entire project can be runned on a Docker image                  


