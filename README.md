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
https://docs.docker.com/engine/reference/run/#clean-up---rm



Use the following command to access the saved results:

```

docker run --rm -t -v "$PWD/results:/opt/sherlock/results" mysherlock-image -o /opt/sherlock/results/text.txt user123

```

The ```-v "$PWD/results:/opt/sherlock/results"``` options tell docker to create (or use) the folder `results` in the

present working directory and to mount it at `/opt/sherlock/results` on the docker container.

The `-o /opt/sherlock/results/text.txt` option tells `sherlock` to output the result.

Or you can use "Docker Hub" to run `sherlock`:

```

docker run theyahya/sherlock user123

```

### Using `docker-compose`

You can use the `docker-compose.yml` file from the repository and use this command:

```

docker-compose run sherlock -o /opt/sherlock/results/text.txt user123

```

## Tests

Thank you for contributing to Sherlock!

Before creating a pull request with new development, please run the tests

to ensure that everything is working great.  It would also be a good idea to run the tests

before starting development to distinguish problems between your

environment and the Sherlock software.

The following is an example of the command line to run all the tests for

Sherlock.  This invocation hides the progress text that Sherlock normally

outputs, and instead shows the verbose output of the tests.

```

$ cd sherlock/sherlock

$ python3 -m unittest tests.all --verbose

```

Note that we do currently have 100% test coverage.  Unfortunately, some of

the sites that Sherlock checks are not always reliable, so it is common

to get response problems.  Any problems in connection will show up as

warnings in the tests instead of true errors.

If some sites are failing due to connection problems (site is down, in maintenance, etc)

you can exclude them from tests by creating a `tests/.excluded_sites` file with a

list of sites to ignore (one site name per line).

## Stargazers over time

[![Stargazers over time](https://starchart.cc/sherlock-project/sherlock.svg)](https://starchart.cc/sherlock-project/sherlock)

## License

MIT © Sherlock Project<br/>

Original Creator - **Siddharth Dushantha**
