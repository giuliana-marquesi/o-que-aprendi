-   Deve ter instalada a biblioteca: **libaio1**. Que pode ser baixada e
    instalada com o comando:

                apt-get install libaio1

    ### Baixando

-   No site: <http://dev.mysql.com/downloads/mysql/> selecionar arquivo
    de acordo com a distribuição e depois a arquitetura da máquina.

-   Será redirecionado para outra página que pedirá para entrar com a
    conta MySQL ou se cadastrar. Selecionar link abaixo “No thanks, just
    start my download”.

    ### Pré-instalando

-   Criar uma pasta qualquer e mover o arquivo baixado para ela.

-   Ir no diretório que salvou o download e fazer o seguinte comando
    para descompactar o arquivo:

                tar -xvf mysql-server_MVER-DVER_CPU.deb-bundle.tar

-   Com o comando:

                dpkg-preconfigure mysql-community-server_*.deb

    Irá configurar a senha do root do servidor. No caso, foi configurado
    como: root1234 (é aconselhado escolher uma senha forte).

    ### Instalando

-   Para uma instalação basica, é preciso instalar os arquivos comuns da
    base de dados, o pacote de cliente, o meta-pacote de cliente, o
    pacote de servidor, e meta pacote de servidor, nesta ordem. Através
    deste comando tudo é resolvido:

        dpkg -i mysql-{common,community-client,client,community-server,server}_*.deb

-   Caso dê algum problema com dependêcias, usar este codigo:

                apt-get -f install

    E depois chamar o código anterior.

    Workbench
    ---------

    ### Notas

-   O site oficial recomenda de usar o repositério apt-get para
    instalar, pois ele resolve problemas de dependências.

    ### Requisitos

-   É necessário inserir o repositório mysql no APT. Para isso é
    necessário baixar o arquivo .deb de site:
    <http://dev.mysql.com/downloads/repo/apt/>.

-   Será redirecionado para outra página que pedirá para entrar com a
    conta MySQL ou se cadastrar. Selecionar link abaixo "No thanks, just
    start my download.

-   Na pasta onde o arquivo foi baixado executar o comando:

                dpkg -i nome-da- versao-especifica-do-pacote.deb

-   Será perguntada qual versão deseja do mysql que deseja instalar como
    repositorio, caso queria a atual ou não sabe (indiferente) apenas
    selecione o “Ok” do menu inicial e mais uma vez o “&lt;Ok&gt;” de
    baixo dando enter.

-   É preciso pegar as chaves públicas do MySQL com o comando:

            apt-key adv --keyserver pgp.mit.edu --recv-keys 5072E1F5 

-   O arquivo source.list geralmente já é criado, porém, dê uma olhada
    neste caminho de arquivo: **/etc/apt/sources.list.d/mysql.list**

-   Caso não exista, colar o seguinte comando dentro:

             deb http://repo.mysql.com/apt/{debian|ubuntu}/
             {jessie|wheezy|precise|trusty|utopic|vivid}
             {mysql-5.6|mysql-5.7|workbench-6.2|utilities-1.4|
             connector-python-2.0}

-   ATENÇÃO! Deve-se arrumar de acordo com sua versão

-   OBS: Alguns pacotes foram ignorados mesmo com a pgp (preciso
    verficar baixando a chave e instalando na mao ela)

-   Para atualizar o APT deve exercutar o comando:

                apt-get update

    ### Instalando

-   Com o comando:

                 apt-get install mysql-workbench

    Workbench ladob
    ---------------

    É possivel baixar o Workbench para sistemas Ubuntu (em outros
    sistemas que usam .deb houve problema com dependências) e também
    pacotes genéricos (**.tar.bz**).

    ### Baixando

-   Em ambos os casos, no site:
    <http://dev.mysql.com/downloads/workbench/> selecionar arquivo de
    acordo com a distribuição e depois a arquitetura da máquina.

-   Será redirecionado para outra página que pedirá para entrar com a
    conta MySQL ou se cadastrar. Selecionar link abaixo “No thanks, just
    start my download”.

    ### Instalando

-   No caso do **.deb** deve usar o código:

                 dpkg -i pacote.deb

    . Se não funcionar, usar o código:

                 apt-get -f install

-   No caso do **.tar.bz** devem ser compilados os arquivos seguindo as
    instruções do README e o INSTALL.

    ### Bugs

-   A instalação do **tarball** falhou em várias distribuições. É
    provavel que seja um bug com o C++.

-   Não foi possível instalar o **.deb** em outras distribuições que
    usam esse gerenciador de pacotes (faltaram dependencias). Não foi
    testado no Ubuntu.

    Windows:
    ========

    MYSQL {#mysql-1}
    -----

    ### Baixando

-   No site: <http://dev.mysql.com/downloads/installer/> selecionar
    arquivo:

-   **mysql-installar-web-community**, se tiver internet enquanto roda o
    installer

-   **mysql-installer-community**, se não tiver internet

-   Será redirecionado para outra página que pedirá para entrar com a
    conta MySQL ou se cadastrar. Selecionar link abaixo “No thanks, just
    start my download.”

    ### Instalando

-   Rodar o arquivo Instaler baixado.

-   Abrirá janela que mostrará como opção escolher instalar o Workbench

-   Aceitar o termo de licença.

-   No próximo passo, deverá escolher o que será baixado e instalado.

-   MySQL Server de acordo com a arquitetura da máquina

-   Neste caso, foi selecionada a documentação, exemplos e modelos

-   Após instalado, ainda na janela do Installer, deverão ser
    configuradas algumas opções.

-   Manter o tipo de configuração: Development Machine

-   Definir a porta TCP/IP de conexão do servidor. Por padrão está 3306.
    (Firewall habilitará uso desta porta se deixar a caixa: " Open
    firewall port for network acess)

-   Definição de senha root. (No caso: root1234)

-   É possível criar um usuário. No caso foi criado o “admin” com host:
    &lt;All Hosts (

-   As configurações de serviço Windows estão configuradas como o padrão
    sugerido:

-   Nome:MySQLtest

-   Com o serviço iniciando com sistema

-   As outras janelas ficaram com a configuração padrão.

    Workbench
    ---------

    ### Pré-requisitos

-   É necessário ter instalado na máquina:

-   Microsoft .NET Framework 4 Client Profile (link:
    <https://www.microsoft.com/pt-BR/download/details.aspx?id=17113>)

-   Visual C++ Redistributable Packages for Visual Studio 2013 (link:
    <https://www.microsoft.com/en-us/download/details.aspx?id=40784>)

    ### Baixando

-   No site: <http://dev.mysql.com/downloads/workbench/> baixar e
    selecionar arquivo referente à arquitetura do computador.

-   Será redirecionado para outra página que pedirá para entrar com a
    conta MySQL ou se cadastrar. Selecionar link abaixo "No thanks, just
    start my download.

    ### Instalando

-   Seguir todos os passos da janela clicando no próximo, lembrar de
    selecionar a caixa de que concorda com os Termos de Licença do
    programa.


