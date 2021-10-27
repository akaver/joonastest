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


sudo docker ps
sudo docker stop streamlit

Mapi väline kataloog sisemiseks kataloogiks
-v väline_kataloog:sisene_kataloog

maps current dir
-v $(pwd):/app

näiteks:
-v /home/ubuntu/minurakendus/:/app


~~~bash
sudo docker run -d -p 80:8080 -v /home/ubuntu/projekt/:/app --name streamlit --restart unless-stopped -ti --rm test:latest streamlit run --serrver.port 8080 minukood.py
~~~

