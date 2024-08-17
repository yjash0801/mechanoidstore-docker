FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
COPY mechanoidstore.conf /etc/nginx/default.d/mechanoidstore.conf
ADD static /usr/share/nginx/html/