FROM nginx:1.7
MAINTAINER Michael A. Smith <msmith3@ebay.com>
COPY nginx.conf /etc/nginx/conf.d/default.conf
ADD run.sh /run.sh
RUN chmod +x /run.sh

#EXPOSE 80
CMD ["/run.sh"]
