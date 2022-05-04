# Comandos básicos

## Ex. com Container Ubuntu

Executa um container Ubuntu:

`$ docker run -i -t ubuntu /bin/bash`

`-i` - interactivity - entre no container

`-t` - terminal

`-d` - detached - não executa no terminal (background)

`--name (nome)`

--

`$ docker ps -a`

`ps` - process status

`-a` - all

--

`$ docker attach (id)`

acessa o container em execução

--

`$ docker stop (id)`

`$ docker rm (id)`

`$ docker images` - exibe as imagens

`$ docker image ls` - exibe as imagens

### - VOLUMES

`$ docker run --read-only -it --name seminarios -v /home/PUCMINAS/68626/anotacoes:/etc/Curso ubuntu /bin/bash`

docker executa (apenas leitura) interativamente, terminal, nome seminarios, cria um volume usando o path A : path B (container)

### - PORTAS

`$ docker run -dp 80:80 docker/getting-started`

`-p` - port

# DOCKER FILE

Start Docker service

`$ sudo systemctl start docker.service`

Run a Docker file

`$ docker build -t (username)/(nomedorepositorio) .`

RUN - comando

CMD - comando apos o build

ENTRYPOINT - durante

ADD - transfere um arquivo para a imagem

EXPOSE - dispõe uma porta

VOLUME - cria um volume

USER - nome do usuario do SO

WORKDIR - seleciona o diretorio para trabalhar

# DOCKER COMPOSE

`$ docker-compose up -d`


# DOCKER HUB

`$ docker login`

`$ docker tag username/original dockerhubusername/quecque` - renomeia a imagem