# lnmp_docker

Docker compose configuration to dockerize Linux+Nginx+Php+Mysql projects.\
Requires Git and Docker installed

Starting new project steps:
1. Create new directory (for example "blank.dev") and fall in
    > mkdir foo.dev && cd blank.dev 
2. Clone "lnmp_docker"
    > git clone https://github.com/IOlenev/lnmp_docker.git
3. Rearange directories
    > mv lnmp_docker/www www && rm -Rf lnmp_docker
4. Modify (skip or do it later) containers names and hostname in files\
    - docker/docker-compose.yml
    - docker/hosts/*.conf
5. Build|Rebuild docker containers
    > cd www/docker && sh build.sh
6. Modify your hosts file by adding your hostnames\
   - 127.0.0.1 blank.dev
   - 127.0.0.1 blank.pma
7. Open
   > http://blank.dev \
   > http://blank.pma:81
8. Done!
9. Based on
   > https://miac.volmed.org.ru/wiki/index.php/Docker-compose_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D0%B4%D0%BB%D1%8F_%D1%81%D0%B0%D0%B9%D1%82%D0%B0_NGINX_%2B_MYSQL_%2B_PHP-FPM