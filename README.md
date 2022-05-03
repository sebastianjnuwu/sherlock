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

Apache License 2.0 © Sherlock Project<br/>

Original Creator - **Siddharth Dushantha**
