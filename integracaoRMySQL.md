-   **Todas as instalações foram feitas pela ferramenta apt-get**

-   Foi instalada a versão mais recente dos Repositórios do Debian 8.5.

-   Versão R-Cran: 3.1.1 (2014-07-10) – “Sock it to Me”.

-   O pacote foi instalado pelo comando:

                        apt-get install r-base
                    

    Instalando pacotes RMySQL e DBI
    -------------------------------

-   Foram instaladas as versões mais recentes dos repositórios do Debian
    8.5.

-   Os pacotes do DBI e RMySQL foram baixados pelo comando:

                    apt-get install r-cran-dbi r-cran-rmysql
                    

-   Versão DBI: 0.3.1

-   Versão RMySQL: 0.9-3

    Instalando o RStudio
    --------------------

-   No site: <https://www.rstudio.com/products/rstudio/download3/>

-   Foi instalada a versão mais recente e estável recomendada para
    Ubuntu/Debian 64bits.

-   Foi baixado o pacote .deb que foir instalado usando os comandos:

                        dpgk -i rstudiopacote.deb
                        apt-get install -f
                        dpkg -i rstudiopacote.deb
                    

-   O comando apt-get foi usado para baixar as dependências faltantes.

-   Versão RStudio: 1.0.136

    Configurando a integração entre R e MySQL
    =========================================

    Conectando à um banco de dados
    ------------------------------

-   Para de conectar deve ser chamado o pacote a ser usado, no caso
    RMySQL.

                        library(RMySQL)
                    

-   Para o RStudio a ligação dos pacotes pode ser feita de forma visual,
    clicando no “Packages” e selecionando o pacote RMySQL.

    ![Carregando pacotes no
    RStudio[]{data-label="fig:pacotes_rstudio"}](carregando-pacotes-rstudio.png){width="\textwidth"}

-   Depois, deve ser carregado o Banco de Dados setado no arquivo para a
    variavel, no caso chamada de con.

-   Por padrão, deve-se realizar uma conexão passando os dados do
    usuario, a senha, o banco e o host.

    ![Iniciando uma conexão
    padrão[]{data-label="fig:Connexao-padrao"}](conexao-padrao){width="\textwidth"}

-   Porém, pode ser um pouco chato fazer isso o tempo todo, a menos que
    salve smepre o estadod e onde parou.

-   Para diminuir o esforço, é possível configurar um grupo de conxao
    dentro do arquivo **my.cnf** do MySQL.

    ### Alteração do arquivo my.cnf

-   No arquivo /etc/mysql/my.cfn foi inseridas as linhas a seguir para
    configurar um grupo

                        [integracaor]
                        #
                        user        = moodleuser
                        password    = 123456
                        host        = 127.0.0.1
                        port        = 3306
                        database    = moodle
                    

-   ele facilita a conexao do R com o MySQL

-   Foi colocado logo apos o grupo default mysqld

-   Para realizar conexão através do grupo basta fazer o seguinte
    comando:

             con <- dbConnect(MySQL(), group="integracaor")
                    

    Comandos de manipulação de tabela básicos
    -----------------------------------------

-   Documentação do RMySQL:
    <https://cran.r-project.org/web/packages/RMySQL/RMySQL.pdf>

-   Mostrar todas as tabelas do Banco de Dados.

                        dbListTables(con)
                    

    ![Integração rodando no R do
    terminal[]{data-label="fig:rmysql_funcionando"}](integracao-RMySQL-funcionando.png){width="\textwidth"}

    Link de base
    ------------

    <http://r.ikasten.io/2011/07/19/receta-integrar-r-y-mysql/>


