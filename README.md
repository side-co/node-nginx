# NODE+NGINX Docker image

## How to use

Copy your nginx configuration in the nginx folder
```
COPY nginx.conf /etc/nginx/nginx.conf
```

Then copy the result of your build into `/usr/share/nginx/html`
```
COPY build/* /usr/share/nginx/html/.
```

Finally, run nginx in your entrypoint:
```
ENTRYPOINT ["nginx", "-g", "daemon off;"]
```
