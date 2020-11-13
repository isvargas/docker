# DOCKER - COMANDOS BÁSICOS

1. Listar imagens:

#docker images

2. Listar containers:

#docker ps -a

3. Baixar uma imagem:

#docker pull debian

4. Gerar um container de uma imagem e cair no shell

#docker run -it debian /bin/bash

onde:

-i: interativo

-t: terminal

debian: nome da imagem

/bin/bash: comando a ser executado

5. Inspecionar um container

#docker inspect CONTAINER_ID

6. Parar/Iniciar um container

#docker stop|start CONTAINER_ID

7. Entrar em um container

#docker attach CONTAINER_ID

8. Gerar uma imagem de um container

#docker commit CONTAINER_ID nome_nova_imagem

9. Remover container

#docker rm CONTAINER_ID -f

10. Remover imagem

#docker rmi nome_imagem

11. Criar um container mapeando um volume local

#docker run -it -v D:\DirLocal:/home debian /bin/bash

Tudo que for colocado na pasta D:\DirLoca aparecerá na pasta /home do container, e vice-versa.

12. Criar um container mapeando portas

#docker run -it -p 80:80 debian /bin/bash

A partir daqui você pode acessar http://127.0.0.1 que vai cair na porta 80 do container.

13. Rodar container em background

#docker run -d imagem


# EXPORTANDO CONTAINERS

1. Salve uma imagem do container

#docker commit CONTAINER_ID nome_imagem

2.Salve em .tar:

#docker save nome_imagem > imagem.tar

3. Envia imagem.tar para o outro servidor.

4. No servidor destino, importar a nova imagem:

#docker load < nome_imagem.tar
