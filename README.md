# StrutsShell
Apache Struts (CVE-2017-5638) Shell

## Introduction

The "**LowNoiseHG (LNHG) Struts Shell**" ("**StrutsShell**" from now on) was conceived in March 2017 after realizing the usefulness of not having to exploit Apache Struts CVE-2017-5638 manually (HTTP GET requests by hand) and after realizing the respective metasploit module for this vulnerability did not work (at least on our test cases).

## Description

The basic operation of **StrutsShell** consists of the processing of a command-line (shell) input for the attacked platform (Windows, Linux, etc.) and using the Apache Struts vulnerability tu push it to the shell to be executed. The tool then returns the answer and waits for the next shell command, providing a flawless interaction experience.

## Special Features

- Input
  - Target needs to be a full vulnerable URL on an Apache Struts server (i.e. http://www.example.com/test/login.action)
- HTTP/HTTPS
  - StrutsShell works automatically with HTTP or HTTPS sites
- Output
  - No output files, this is an interactive shell (not really, just a graphical representation of one, no real tty)

## Parameters
```
# LowNoiseHG Apache Struts (CVE-2017-5638) Shell v.0.1 (2017/03/17)
# by F4Lc0N - LNHG - USA/Colombia
#
# Thanks to Andrew Weidenhamer (@AWeidenhamer), David Llorens (c4an),
# Tauseef Ghazi (@tghazi), and AJ (@nikamajinkya) for inspiration, ideas
# and debugging/betatesting help.

usage: StrutsShell.py [-h] [-d] [-u URL]

LNHG Apache Struts (CVE-2017-5638) Shell v.0.1

optional arguments:
  -h, --help         show this help message and exit
  -d, --debug        show debugging info
  -u URL, --url URL  Apache Struts vulnerable URL (i.e.:
                     http://www.example.com/test/login.action)
 for inspiration, ideas and debugging/beta-testing help.

```
## Current State of Development

As most of the R&D done in **LowNoiseHG (LNHG)** this tool was designed and developed only for its usefulness and with no economic funds or time allocated to it. All development has been done on personal time only, and it will continue as interesting featurs come up, and if time is available taking into account other projects.

The current version works very well, even though there are still some minor wrinkles (bugs) to iron, and some basic features that can be improved.
 
## License

**StrutsShell** and all its related code is released under the **GPL v3 open-source license**. The full license is attached in the LICENSE.md file.

## Requirements

In order to run **StrutsShell** "out-of-the-git", with all options enabled, you will need:

- Python - Programming language (sudo apt-get instal python)
- requests - Python module (pip install requests)

**NOTE: StrutsShell** was developed and tested on Kali, Ubuntu and Debian. I am sure **YOU** can make it work in other platforms of your choice ;)

## Installation

### Install required software with apt-get:
```
$ sudo apt-get install -y python git
$ pip install requests
```

### Install **StrutsShell**
```
$ cd /opt
$ sudo git clone https://github.com/falcon-lnhg/StrutsShell.git
$ cd StrutsShell
```
## Running (Example)
```
$ ./StrutsShell.py -u http://www.example.com/test/login.action
```
You can check the full list of options at any time with:
```
$ ./StrutsShell -h
```
## Example Screenshot
![Alt text](https://raw.githubusercontent.com/falcon-lnhg/StrutsShell/master/screenshot.jpg "StrutsShell - Example Screenshot")

## Developer Team

### [LowNoiseHG] (http://www.lownoisehg.org):

- F4Lc0N - falcon [at] lownoisehg.org
