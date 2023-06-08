## Local Deployment on Windows

In order to run project localy, do the following steps:
1. edit hosts file
  - go to `C:\Windows\System32\drivers\etc` dir;
  - open `hosts` file;
  - add in the end of the file:
    ```
    127.0.0.1 app.loc
    127.0.0.1 api.app.loc
    ```
  - save the file.
2. clone project from the repo
3. install docker by using the link: https://docs.docker.com/desktop/install/windows-install/
4. open `cmd`
4. go to folder with the project `cd path_to_project\axisbits`
5. run the command `docker-compose -f docker-compose.local.yml up -d`

## Dev Env Deployment on Linux

In order to erun project on DEV-server, follow the instructions:
#### Prerequisites:
 - DNS records should be created and attached to DEV-server IP

1. set proper valiues for `DNS_FRONTEND` and `DNS_BACKEND` vars in `.env` file
2. install `git`:
  - `sudo dnf install git-all` (for CentOS/Fedora)
  - `sudo apt-get install git-all` (for Debian/Ubuntu)
3. clone the project
4. go to the dir with project `cd path_to_project/axisbits`
5. run the command `docker-compose -f docker-compose.dev.yml up -d`

## Useful commands
- `docker ps` - list of running containers
- `docker exec -it container_name bash` - connect to the container and/or execute commands
- `docker logs -n30 -f container_name` - show logs of the container in real-time mode
