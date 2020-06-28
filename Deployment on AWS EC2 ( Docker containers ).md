# Deployment on AWS EC2 ( Docker containers )

[Reference](https://medium.com/@umairnadeem/deploy-to-aws-using-docker-compose-simple-210d71f43e67)

1. Launch your ec2 instance.
2. Get your key
3. SSH into your instance ```ssh -i "key.pem" ec2-user@ec2-3-11-11-144.us-east-2.compute.amazonaws.com```
4. Install Nodejs, Docker there
5. git clone your repo 
6. Docker build ```docker-compose up --build -d```
7. Open ports in security group. ( Each VM has own security group remember to open ports of that VM )
8. Should work, change apis domain to ec2's if required.


Some Docker commands 

```
docker-compose up --build -d
docker run --name docker-nginx -p 80:80 nginx
docker stop docker-nginx
docker rm docker-nginx
docker exec -it [container-id] bash
docker exec -it cff58196dd9d nginx -s reload
```