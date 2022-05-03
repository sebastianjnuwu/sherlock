# SHERLOCK 

![](https://raw.githubusercontent.com/sherlock-project/sherlock/master/images/sherlock_demo.gif)

# Installation
```
# clone the repo
$ git clone https://github.com/sebastianjnuwu/sherlock

# change the working directory to sherlock
$ cd sherlock

# install the requirements
$ python3 -m pip install -r requirements.txt
```

# Usage
```
$ python3 sherlock --help
```
To search for only one user:
```
python3 sherlock user123
```
To search for more than one user:
```
python3 sherlock user1 user2 user12
```
Accounts found will be stored in an individual text file with the corresponding username (e.g `user123.txt` ).

# Anaconda (Windows) Notes

If you are using Anaconda in Windows, using 'python3' might not work. Use 'python' instead.

# Docker Notes

If docker is installed you can build an image and run this as a container.
```
docker build -t mysherlock-image .
```
Once the image is built, sherlock can be invoked by running the following:
```
docker run --rm -t mysherlock-image user123
```
The optional `--rm` flag removes the container filesystem on completion to prevent cruft build-up. See:
