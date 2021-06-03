# Login :

This service is written on Golang.

Create a user for running the application

```
  #apt update

  #useradd -m -s /bin/bash todoapp

  #cd /home/todoapp/
```

Run the following command as a user with sudo privileges to download and extract the Go binary archive in the /usr/local directory:

```
  #wget -c https://dl.google.com/go/go1.14.2.linux-amd64.tar.gz -O - | sudo tar -xz -C /usr/local
```

Verify the installationby simply runningthe command go version.

```
  #go version 
```

The output should look something like this:

```
output:
go version go1.14.2 linux/amd64

```
By adding the location of the Go directory to the $PATH environment variable, the system will know where to find the Go executable binaries.

This can be done by appending the following line either to the /etc/profile file (for a system-wide installation) or the $HOME/.profile file (for a current user installation):

```
  #~/.profile

  #export PATH=$PATH:/usr/local/go/bin
```

Save the file, and load the new PATH environment variable into the current shell session:

```
  #source ~/.profile
```

By default, the GOPATH variable, which specifies the location of the workspace is set to $HOME/go. To create the workspace directory type:

```
  #mkdir ~/go
```

Inside the workspace create a new directory /src

```
  #mkdir -p ~/go/src

  #cd  ~/go/src/
```

Lets clone the code from github repository 

```
  #git clone https://github.com/zelar-soft-todoapp/login.git

  #cd login/

  #apt update
```
Navigate** to the ~/go/src/login/login directory and run go build to build the program:

```
  #apt install go-dep

  #go get

  #go build
```

NOTE: Configure below environment variable

```
  #export AUTH_API_PORT=8080

  #export USERS_API_ADDRESS=http://172.31.16.229:8080
```
Finally start the Login Module once to effect the changes by the below cammand.

```
  #./login
```
;)
# RELEASE 0.0.1 -DATE - 03-06-2021