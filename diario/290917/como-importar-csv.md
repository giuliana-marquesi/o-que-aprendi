# Como importar arquivos csv para uma tabela #

## Arquivo de configuração ##

As novas versões de MySQL possuem uma variável de ambiente própra que determina qual diretório é considerado seguro. Desta forma, ele impede a importação de outros locais.

Sendo assim, num ambiente que não de produção, é possível modificar o arquivo de configuração do MySQL para que se torne "inseguro" e permita ler de qualquer diretório.

O arquivo está no caminho:

> /etc/mysql/my.cnf

### Parar serviços ###

Antes de realizar a modificação, deve-se parar o sistema.

No Debian (8) para parar o processo foi logado na conta root e realizado o comando:

> service mysql stop

### Alterar arquivo ###

Com o arquivo **my.cnf**, alterar o valor, ou no caso inserir abaixo do **[mysqld]** a seguinte informação:

> secure_file_priv = ""

**! ATENÇÃO PARA NÃO COLOCAR ESPAÇO ENTRE AS ASPAS, ISSO CAUSOU ERRO QUANDO TESTEI !**

### Iniciar serviços ###

Depois da alteração, deve-se iniciar o serviço do mysql novamente. Para isso:

> service mysql start

## Query de importação ##

### No Workbench ###

Para que o botão de importação no Workbench apareça disponível é preciso ter necessariamente uma Chave-Primária

![Botão de importar do Workbench](~/Imagens/importar-tabela-workbench.png)

### Formatação do arquivo csv a ser importado no Workbench ###

- Não possuir cabeçalho
- Assegurar que os separadores sejam vírgulas (,) e não ponto-e-vírgula (;)
- **E muito importante: assegurar que as colunas da tabela sejam as mesmas que as do arquivo**

- Depois de garantidas essas formatações, basta utilizar o botão de importação informado no item anterior

### Query de importação via texto ###

O comando que funcionou para o arquivo exportado em questão foi:

> LOAD DATA LOCAL INFILE '~/importar-csv/arquivo.csv' INTO TABLE TABELA FIELDS TERMINATED BY ';' ENCLOSED BY '"' LINES TERMINATED BY '\R\N' IGNORE 1 LINES;
