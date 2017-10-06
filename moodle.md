-   O moodle que usamos é o 3.0

-   <https://download.moodle.org/releases/supported/>

    Requerimentos
    =============

-   Moodle upgrade: Moodle 2.7 or later (if upgrading from earlier
    versions, you must upgrade to 2.7.14 as a first step)

-   PHP version: minimum PHP 5.4.4 (always use latest PHP 5.4.x , 5.5.x
    or 5.6.x on Windows - http://windows.php.net/download/). PHP 7 is
    supported but has some engine limitations.

-   Ghostscript should be installed for pdf annotation.

-   Unoconv should be installed for file conversion used by pdf
    annotations (new in Moodle 3.1)

-   New requirement for Moodle 3.1 comparing to 3.0: PHP extension
    xmlreader

-   Lembrar de instalar o php cURL

                apt-get install php5-curl
            

-   Instalar: php5-xmlrpc libapache2-mod-php5 php5-mcrypt php5-gd
    php5-mysql php5-gd

    instalação
    ==========

-   link que serviu de base para a instalação:
    <https://www.youtube.com/watch?v=UyFEbekhosY> e
    <https://docs.moodle.org/31/en/Installing_Moodle#Set_up_your_server>

    Seguindo os passo a passo
    -------------------------

-   Instalar php5, mysql e apache2 (que é instalado junto com o php5, na
    verdade)

    ### Configurar e criar uma base de dados no MySQL

-   Criar uma base de dados chamada ’moodle’

            CREATE DATABASE moodle DEFAULT CHARACTER SET utf8 COLLATE 
            utf8_unicode_ci;
                

-   Adicionar e dar permissao para usar a bd ’moodle’ a um novo usuário

-   **ATENÇÃO!!**

-   **Este comando de criação de usuário será descontinuado na próxima
    versão do MySQL.**

            GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,CREATE TEMPORARY
            TABLES,DROP,INDEX,ALTER ON moodle.* TO moodleuser IDENTIFIED
            BY '123456';
                

    ### Criar uma pasta dentro do www/html

-   Deve ser copiado o arquivo moodle-versao.tar\* para a pastar do
    servidor web (/var/www/html)

            mv /home/usuario/Downloads/moodle-latest-30.tgz /var/www/html/
                

-   Entrar na pasta /var/www/html e extrair o conteúdo do arquivo
    moodle-versao.\*

            cd /var/www/html
            tar -xf moodle-versao.*
                

    ![image](extraindo-moodle.png) 

    ### Criar uma pasta ’moodledata’

-   Coloquei o moodledata na /var/www/

-   Mudar as permissoes da pasta

            mkdir /var/www/moodledata
            chmod 0777 /var/www/moodledata
                

    ### Dar permissao de uso para o usuario www-data

            chown www-data /var/www/html/moodle/
                

    ### No navegador: digitar localhost/moodle

-   Irá redirecionar para a página de instalação do Moodle em modo
    gráfico

    ![Instalacao
    gráfica[instalacao-1.png)

    ![Configuracao do banco de
    dados](configuracao-bd.png)

    ![Configurando
    Administrador](configuracoes-adm.png)

    O que foi configurado na instalação
    ===================================

    Banco de Dados
    --------------

-   Foi criado o um banco de dados chamado “moodle”

-   Foi criado um usuario MySQL chamado moodleuser com senha 123456

    Instalação Moodle
    -----------------

-   O usuário root do moodle é admin

-   Com nome: Administrador e sobrenome: admin-Sobrenome

-   A senha Root-1234

-   email: email@email.com.br

-   nome do site: Nomedosite 

-   O IP de localhost para acessar o apache2 é: 10.0.2.15/moodle – Isto
    é anotação da primeira instalação, não se fez necessário,a
    princípio, saber este dado.


