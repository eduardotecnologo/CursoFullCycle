## Comandos Unix

- $echo $(pwd) (Mostra o caminho local)

## Lista containers ativos

- $docker ps

## Lista os volumes

- $docker volume ls
- $docker volume create myvolume (Cria um volume)
- $docker run -d --name nginx -d --mount type=volume,source=myvolume,target=/app nginx (Create volume)
- $docker volume prune (mata tudo)

## Lista containers que já foi executado

- $docker ps -a

## Baixa uma imagem caso não exista

- $docker run NAME_IMAGEM
- $docker run -it ubuntu:latest bash (
    -it modo iterativo - libera o terminal para digitar
    -bash - abre no bash ex: root@5618afdedcd5:/#)

## Iniciar Container

- $docker start NAME
- $docker run -it --rm ubuntu:latest bash (
    --rm qdo sair, remove o container automático)
- $docker stop NAME (par um container)
- $docker rm NAME (Remove um conainer, -f força)

## Baixando nginx

- $docker run nginx
- $docker run -d -p 8080:80 nginx (
    -d libera o terminal, -p publica porta 80)
- $docker run -d --name nginx nginx (--name label da imagem)
- $docker run -d --name nginx -d -p 8080:80 nginx
- $docker exec nginx ls (exec executa um conando dentro da imagem)

## Montando um volume compartilhado

- $docker run -d --name nginx -p 8080:80 -v /home/edudeveloper/developer/CursoFullCycle/Docker/html/:/usr/share/nginx/html (Modo antigo)
- $docker run -d --name nginx -p 8080:80 --mount type=bind,source="$(pwd)"/html,target=/usr/share/nginx/html nginx

- $docker rm $(docker s -a -q) -f (Remove a listade imgens peli id)
