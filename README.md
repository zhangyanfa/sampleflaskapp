
### Overview
 This code is a fork of the following [code](https://github.com/jay3dec/PythonFlaskMySQLApp---Part-1) and is used to demonstrate dockerized deployment.
 Explanation of the code is provided [here](http://code.tutsplus.com/tutorials/creating-a-web-app-from-scratch-using-python-flask-and-mysql--cms-22972)

### Build

To build this for ppc64le arch, do the following:

    `docker build -t ppc64le/flaskapp -f Dockerfile.ppc64le .`
     
### Deploy in a Kubernetes cluster

 - Install the `helm` CLI and ensure it's working against your kubernetes cluster. 
 - Ensure that you have a mariadb service running.
 - Simply clone the repository and run the following from the `sampleflaskapp` directory:

    `helm install --name demoapp helmchart`
