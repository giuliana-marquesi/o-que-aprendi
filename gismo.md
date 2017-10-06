-   Na página: <https://bitbucket.org/steveorulez/block_gismo/downloads>

-   Descompactar o arquivo zip.

    Instalando
    ----------

-   Copiar (ou mover) para a pasta **/var/www/html/moodle/blocks**

-   Logar no Moodle com o Administrador. Clicar no botão “Personalizar
    esta página” na página principal.

-   Será redirecionado para outra página que informará que existe o
    GISMO para instalar como plugin.

-   No fim da página, há o botão “Atualizar agora”, clicar nele.

-   Após o carregamento da atualização, surgirá as configurações do
    GISMO. Já está setado um padrão (que foi mantido).

    Configuração
    ============

    Exportar dados pela primeira vez
    --------------------------------

-   O GISMO precisa exportar os logs do Moodle para que consiga fazer os
    gráficos e análises.

-   Geralmente está agendado no *cron* para rodar a extração as 2 da
    manhã.

-   No readme do GISMO há instruções do que deve ser feito:

    -   Deve ir em administrção do site - Servidor - Terafas agendadas

    -   Clicar no Editar na linha correspondente ao block GISMO

-   Porem, isso só altera a ora. Para sincronizar imediatamente deverá
    ir na pasta **moodle** e executar este comando:

            php admin/tool/task/cli/schedule_task.php

            --execute=\\block_gismo\\task\\export_data
            

-   O arquivo: README.txt

    Colocando o block GISMO no curso
    --------------------------------

-   O block do GISMO deve ser colocado no curso escolhido.

-   Primeiro deve-se ativar a edição, como administradora

-   Na página de administração do curso, no canto inferior esquerdo
    existe o campo **“ADICIONAR UM BLOCO”**.

-   Escolher o GISMO.

    Usando o GISMO
    ==============

    Primeira vez
    ------------

-   Na página do curso, clicar no link “Reporting Tool”, no canto
    inferior esquerdo.

-   Será aberta outra aba.

    AVALIAÇÃO DA FERRAMENTA
    =======================

    Como funciona
    -------------

-   A ferramenta pega os logs do curso e realiza cálculos estatísticos.

-   Os professores e os administradores do curso podem ver a performance
    geral da classe.

-   Os alunos podem ver suas próprias estatísticas e dados.

    Pontos Positivos
    ----------------

-   É um block próprio do Moodle. (Funciona dentro dele)

    Pontos Negativos
    ----------------

-   A ferramenta é em inglês

    ANEXO
    =====

    **Documentação:** <http://gismo.sourceforge.net/>

    **Tutoriais sugeridos pela documentação:**
    <http://moclog.ch/tutorials/>


