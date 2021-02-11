# webdav
Ejemplo docker-compose:

  webdav:
    image: adanton/webdav:armv7
    container_name: webdav
    restart: unless-stopped
    ports:
      - 85:80
    volumes:
      - $HOME/webdav:/var/lib/dav
    environment:
      - AUTH_TYPE=Basic
      - USERNAME=webdav
      - PASSWORD=webdav
