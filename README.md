# joonastest

buildi image:

~~~bash
sudo docker build -t test .
~~~

jooksuta interaktiivselt

~~~bash
sudo docker run -p 80:8080 --name streamlit -ti --rm test:latest
~~~

-p väline_port:sisene_dockeri_port

Jooksuta taustal

~~~bash
sudo docker run -d -p 80:8080 --name streamlit --restart unless-stopped -ti --rm test:latest
~~~
