This code is a fork of the following [code](https://github.com/jay3dec/PythonFlaskMySQLApp---Part-1) and is used to demonstrate dockerized deployment.
Explanation of the code is provided [here](http://code.tutsplus.com/tutorials/creating-a-web-app-from-scratch-using-python-flask-and-mysql--cms-22972)

#Build
 docker build -t flaskapp .
  
 For building it on PowerPC LE platform do this
 docker build -t ppc64le/flaskapp -f Dockerfile.ppc64le .
     
#Run
 docker run -itd -e MYSQL_USER=user -e MYSQL_PASSWORD=pass -e MYSQL_DB=test --link mysql:db  -p 8080:80 flaskapp

