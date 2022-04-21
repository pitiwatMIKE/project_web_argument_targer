# Project Web Argument Targer

![Screenshot 2022-04-21 164501](https://user-images.githubusercontent.com/68042822/164428209-9acf0aaa-91cf-4d17-baa4-4efbdda83553.png)

# Installation

## Install in local

Creating virtual environments
```
sudo apt update
sudo apt install python3.8
python3.8 -m venv env_web_argument
```

Activating a virtual environment
```
source env_web_argument/bin/activate
```

Clone Project
```
git clone https://github.com/pitiwatMIKE/project_web_argument_targer.git
```

install packages requirements
```
cd project_web_argument_targer
pip install -r requirements.txt
```

Run web application
```
python3 app.py
```

## Install on unbuntu server with docker
**install docker**
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

Clone project
```
git clone https://github.com/pitiwatMIKE/project_web_argument_targer.git
cd project_web_argument_targer
```

Using docker build
```
sudo docker build --tag web-argument-targer .
```

Docker run
```
sudo docker run -d -p 80:5000 web-argument-targer
```
***Success fully!! <br/>***
***wait about 2 minutes <br/>***
***You can go see Web Applications at your Public Ip***
<br/>
### If you want to use Domain name instead of public Ip
Follow the steps below.
```
cd project_web_argument_targer
```

```
vi static/js/fetch_api.js
```

At project_web_argument_targer/static/js/etch_api.js
```
# in line 2
const host = window.location.protocol + "//" + window.location.host;
# change to
const host = "http://example.com";
```

Copy <CONTAINER ID>
```
sudo docker ps
```
  
Change file fetch_api.js in docker
```
sudo docker cp static/js/fetch_api.js <CONTAINER ID>:/python-docker/static/js/fetch_api.js
```

Restart container
```
sudo docker restart <CONTAINER ID>
```
  







