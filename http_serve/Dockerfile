# docker build -t vincd:http_serve .
# docker run -it --rm -v $PWD:/pwd -p 8000:80 vincd:http_serve

FROM nginx:stable

COPY default.conf /etc/nginx/conf.d/
COPY nginx.sh /
ENTRYPOINT [ "/nginx.sh" ]
