-   Na página: <http://community.pentaho.com/projects/reporting/>

-   Deve Fazer o download para seu SO, nocaso, Linux.

-   Descompactar os arquivos. É criada uma pasta chamada
    **report-designer**

    Dependências
    ------------

    ### Java

-   Na documentação é dito que se faz necessário o uso do java jdk e jre
    1.5 e 1.6 pelo menos.

-   Porém, com o Java 7 OpenJDK não funcionou. Foi instalado o OpenJDK 8
    e o programa rodou.

-   Se preciso instalar o Java 8 da Oracle, pode-se usar um repositório
    de binários externo.

-   Seguindo o tutorial do link:

    [http://www.edivaldobrito.com.br/como-instalar-o-oracle-java-8-em-debian\\-via-repositorio/](http://www.edivaldobrito.com.br/como-instalar-o-oracle-java-8-em-debian\-via-repositorio/)

    ### Instalando Driver MySQL

-   Apesar da documentação dizer que ja vem com o driver do MySQL, não
    foi possível realizar conexão apenas com o programa puro

-   No site: <http://dev.mysql.com/downloads/connector/j/>

-   Realizar download do arquivo (independente do formato escolhido)

-   Descompactar o arquivo baixado.

-   Copiar arquivo **.jar** para a pasta:

                /report-designer/lib/jdbc
            

    Rodando o programa
    ==================

-   Na pasta **report-designer** existe o executável:

                report-designer.sh
            

-   apenas execute ele. Com dois clique no modo gráfico. Ou no terminal
    usando **./report-designer.sh**

    Criando uma conexão com o banco de dados
    ========================================

-   Com o programa já aberto. Ir no menu superior no caminho:

                Data -> Add Datasource -> JDBC
            

-   Abrirá uma janela nova. Nela o caminho é:

-   Clicar no botão verde +

-   Abrirá uma outra janela

-   No campo Connection Type. Escolher MySQL

-   No campo Access. Escolher JDBC

-   Seguir o modelo a seguir:

    ![Criando uma conexao com o
    Moodle](conexao-jdbc)


