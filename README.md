# Introduction

This repository contains a short tutorial for Polymer 1.x.

# Installation

The following chapter describes the installation process of NPM and bower. This steps 
needs to be done only once.

## 1. Install node js for NPM package manager 

Download and install nodejs from [nodejs.org](https://nodejs.org)

## 2. Setup proxy for NPM

```cmd
    npm config set proxy http://user:password@proxy.company.com:8080
    npm config set https-proxy http://user:password@proxy.company.com:8080
```

## 3. Install bower and polymer-cli

```cmd
    npm install -g bower
    npm install -g polymer-cli
```

## 4. Set proxy environment variables for bower from powershell

```cmd
[Environment]::SetEnvironmentVariable("http_proxy", "http://user:password@proxy.company.com:8080", "User")
[Environment]::SetEnvironmentVariable("https_proxy", "http://user:password@proxy.company.com:8080", "User")
```

# Usage

The following chapter describes the steps required to install every project specific
dependencies. This steps must be executed for each project.

## 1. Install project dependencies 

```cmd
cd lessonXXX
bower install
```

This command will create a bower_components folder with necessary dependencies.

## 2. Start web server

```cmd
polymer serve
```

The result output will be something like:

```
Starting Polyserve...
    serving on port: 8081
    from root: d:\Private\polymer\lesson001

Files in this directory are available under the following URLs
    applications: http://localhost:8081
    reusable components: http://localhost:8081/components/my-polymer-tutorial/
```

## 3. Open the url provided by polymer serve in a browser

```cmd
chrome http://localhost:8081/components/my-polymer-tutorial/
```

## 4. Start coding

# Troubleshooting

## Not able to download data

Check your proxy settings, check whether you provided user name and password as well.

## Browser did not displayed anything

Ensure that url contains the trailing /

Correct: http://localhost:8081/components/my-polymer-tutorial/
Incorrect: http://localhost:8081/components/my-polymer-tutorial

