# haproxy
haproxy

1) cd into the repo and execute "docker-compose up --build". This will bring up 
  a) Two containers hosting apps web1 and web2. Both these apps are listening to container ports 80
  b) haproxy container which listens to port 80 and and forwards the request as per the below rules
    i) If the path begins with web1, it is forwarded to backend web1:80
    ii) If path begins with web2, it is forwarded to backend web2:80
    iii) If path does not contain web1 or web2 it is forwarded to default backend web1:80


2) Basically localhost/web1 --> localhost:81 and localhost/web2 --> localhost:82

3) Ctrl+C will stop all the three containers

4) "docker-compose down" will remove all the three containers

5) Look at https://www.haproxy.com/blog/the-four-essential-sections-of-an-haproxy-configuration/ to get an overview of the haproxy configuration structure 

