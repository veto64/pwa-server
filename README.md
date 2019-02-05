# Certificated https web server to serve Progressive Web Apps

The main repository is on:

[https://calantas.org/pwa-server/](https://calantas.org/pwa-server)

<img src="https://openclipart.org/download/212488/the_pencil_fist__vector__by_mondspeer-d8d6wtk.svg" width="250">

## Setup
1. Get lets encrypt certificated files from calatans.org by running:
```bash
 ./update_certs.sh
```

2. Edit your hosts file so pdw.calantas.org will link to your local machine 
```bash
sudo sed -i "2i127.0.0.1  pdw.calantas.org" /etc/hosts
```

3. run docker-compose to start the apache ssl webserver 
```bash
docker-compose up -d
```

## License
GNU General Public License v3.0 -






