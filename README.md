# rC3 Generator
![Screenrecording of usage](https://raw.githubusercontent.com/bleeptrack/rc3-generator/main/img/screenrec.gif)

[Live Version](https://rc3.bleeptrack.de)   
[Official Styleguide for rC3 by KREATUR WORKS](https://styleguide.rc3.world/RC3%20Style%20Guide%20Essentials.pdf)

## Develop local with Docker
### Get node modules
To run the application, npm modules are needed.
```bash
# goto repository root directory and enters the command
docker run --rm -v $PWD:/getnmpmoduls node /bin/sh -c 'cd /getnmpmoduls && npm install'
```

### Run http server
To test the application, run a ngnix webserver

```bash
# goto repository root directory and enters the command
docker run --name rc3-generator -p 8888:80 -v $PWD:/usr/share/nginx/html:ro -d nginx
```

Now request the rc3-generator with [http://localhost:8888](http://localhost:8888)

```bash
# Stop and remove the container
docker rm rc3-generator -f
```

### Docker Desktop for macOS and Windows
To run docker on your Mac or Windows, the easiest way is to install [Docker Desktop](https://www.docker.com/products/docker-desktop).



