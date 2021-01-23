FROM ubuntu:latest  
RUN apt-get update  
RUN apt-get install -y nginx 
RUN rm /etc/nginx/sites-enabled/default
#COPY ./hosts/mysite.local.conf /etc/nginx/sites-enabled/mysite.local.conf
COPY ./hosts/mysite.local.conf /etc/nginx/sites-available/mysite.local.conf
RUN ln -s /etc/nginx/sites-available/mysite.local.conf /etc/nginx/sites-enabled/mysite.local.conf
WORKDIR /data  
VOLUME /data  
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]