# Teste de Sistemas Operativos - Módulo 3

Faz *fork* do repositório para teres a tua cópia.

Preenche o ficheiro README diretamente no GitHub. A partir da página principal do repositório, clica em "Edit File" (ícone representando um lápis).

Escreve as respostas dentro dos blocos correspondentes. Substitui as reticências pelo que é pedido em cada pergunta. Não desformates o documento.

Quando acabares, carrega no botão "Commit Changes".

## Informação do aluno

    Nome: Frederico Bacar

## P1 - Para as seguintes questões, assinala a opção correta: (2.5v)

  1. Qual das seguintes afirmações caracteriza melhor um SO servidor?

    a) Projetado para computação de uso geral
    b) Otimizado para alta disponibilidade e confiabilidade
    c) Destinado a usuários individuais
    d) Usado principalmente para jogos
    
    Resposta: b)

  2. Das seguintes, qual é a função mais apropriada para um SO servidor?

    a) Executar aplicações de desktop
    b) Desenvolver aplicações móveis
    c) Fornecer software de entretenimento
    d) Gerir recursos e serviços de rede
    
    Resposta: d)
   
  3. Qual dos seguintes é um sistema operativo servidor popular?

    a) Windows 11
    b) macOS Big Sur
    c) Ubuntu Server
    d) Android
    
    Resposta: c)

  4. Qual é o papel de um servidor num modelo cliente-servidor?

    a) Consumir recursos fornecidos pelos clientes
    b) Fornecer recursos e serviços aos clientes
    c) Atuar como uma estação de trabalho independente
    d) Facilitar a comunicação ponto a ponto
    
    Resposta: a)

  5. Qual dos seguintes protocolos é mais usado para aceder remotamente a servidores?

    a) FTP
    b) HTTP
    c) SSH
    d) SMTP
    
    Resposta: c)

## P2 - Indica, sequencialmnente, os comandos para realizar as seguintes instruções: (7.5v)

  1. Cria um diretório com o nome "ex1", entra no mesmo, e cria 3 ficheiros vazios com os nomes "f1", "f2", "f3". No fim, lista os conteúdos do diretório atual.

    Resposta:
    //Criar diretorio -> mkdir ex1
    //Entrar no diretorio -> cd ex1
    //Criar os ficheiros -> touch f1, touch f2, touch f3
    //listar os conteúdos do diretório atual -> ls
    
  2. Assumindo que estás no diretório "ex1", renomeia os ficheiros "f1" e "f2" para que acabem com "_antigo", e cria cópias dos mesmos.

    Resposta:

    Estou no diretório ex1
    //Renomear os ficheiros "f1" e "f2" para que acabem com "_antigo" -> mv f1 f1_antigo, mv f2 f2_antigo
    // Copiar os ficherios "f1_antigo" "f2_antigo" -> cp f1_antigo f1_antigocopy, cp f2_antigo f2_antigocopy 
    

  3. Assumindo que estás no diretório "ex1", cria o diretório "ex2", e move os ficheiros copiados no exercício anterior para o novo diretório. Seguidamente, apaga os ficheiros originais.

    Resposta:
    //Criar o diretório "ex2" -> mkdir ex2
    //Mover os ficheiros copiados para o novo diretório -> mv f1_antigocopy /ex2, depois mv f2_antigocopy /ex2
    //Apagar os ficheiros originais -> cd.., depois rm f1_antigo, depois rm f2_antigo

  4. Atualiza os repositórios de *packages* para garantir acesso às *packages* mais recentes, e instala o serviço **htop**.

    Resposta:
    //Para atualiazr os repositórios de *packages* para garantir acesso às *packages* mais recentes -> sudo apt update
    //Instalar o serviço htop -> sudo apt install htop

  5. Cria um novo utilizador com o teu primeiro nome, e com o diretório "/home/nome_de_utilizador". Mostra a informação (ID) do utilizador criado.

    Resposta:
    //Criar novo utilizador com diretório -> sudo adduser Frederico --/home/Frederico
    //Mostrar o ID -> id Frederico
## P3 - Realiza os seguintes exercícios, com respostas detalhadas: (6v)

  1. Indica alguns aspetos que diferenciam um SO cliente de um SO servidor.

    Resposta:
    Um SO cliente é mais para um uso nornmal do computador, para uso geral, para uso básico e que o computador não precise de ficar ligado o tempo todo, já o SO servidor é mais para fornecer serviços online, seja um site, um servidor para um jogo ou algum serviço em que a máquina tenha que ficar ligada durante dias para que o serviço funcione otimizado evitando quebras de energias.
     
  2. Explica a importância de otimizar um sistema operativo servidor, com exemplos de técnicas para otimização.

    Resposta:
    A importância de otimizar um sistema operativo servidor é para que a máquina fique mais rapida e tenha um funcionamneto melhor, uma das técnicas para otimização pode ser não deixar a máquina sobreaquecer, pois isso poderá fazer com que funcione mal e também não instalar serviços inúteis para que a memória RAM não precise de executá-los sem motivo.

  3. Descreve o processo de instalar e configurar um servidor web num SO servidor, incluindo as etapas necessárias.

    //Primeiro verificar se está tudo atualizado -> sudo apt update
    //Instalar o apache -> sudo apt install apache2
    //Antes de testar o Apache, é necessário modificar as configurações do firewall para permitir o acesso externo às portas Web padrão -> sudo ufw app list
    //Ativar o Apache -> sudo ufw allow 'Apache'
    //Verificar as mudanças -> sudo ufw status
    //Verificar se o apache está a funcionar corretamente -> sudo systemctl status apache2

    //Se tudo funcionou como devia, já tem o appache instalado com sucesso.
    

## P4 - Indica os comandos **git** para realizar as seguintes operações: (4v)

  1. Considera que estás no ramo 'master' de um repositório git criado localmente. Associa este repositório ao repositório remoto contido no url 'https://github.com/SO/OMeuRepositorioRemoto'. Altera o nome do ramo atual para 'main', e envia os *commits* já feitos localmente para o repositório remoto.

    // Associar o repositorio ao repositorio remoto contido no url -> git remote add origin https://github.com/SO/OMeuRepositorioRemoto
    // Alterar o nome do ramo atual para 'main' -> git branch -m master main
    // Enviar os commits -> git push -u origin main

  2. Considera que estás na pasta raiz do teu repositório local, onde atualizaste um ficheiro de nome 'index.html'. Envia **apenas** esta atualização para o teu repositório remoto, com uma mensagem de commit apropriada.

    //Enviar esta atualização para o repositório -> git commit -m "Atualização do arquivo index.html"
    //Atualizar -> git push origin main
