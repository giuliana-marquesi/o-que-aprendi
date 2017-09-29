# VIM #

## JANELAS ##

+---------------------------------------+-----------+
| cria uma nova janela			        | com :split |
| abre outra janela VIM, acima da atual	| ^wn    |
| desce para outra janela  VIM		    | ^wj    |
| sobe para outra janela VIM		    | ^wk    |
+---------------------------------------+-----------+

## MODOS ##

+---------------------------------------+-----------+
| modo normal no modo insert	        | ^o	       |
| modo visual de bloco			        | nor v + ^v|
| salvar como                           | com :sav "nomearuivo"|
+---------------------------------------+-----------+

## CARACTERES ##

+---------------------------------------+-----------+
| substitui um caracter por outro	    | nor r|
| junta linha atual e abaixo com esp	| nor J|
| muda o CASE dos caracteres (x = nº)	| nor x~|
| deleta caracter à esquerda		    | nor X|
| apaga caracteres e entra modo inseção	| nor s|
| apaga linha toda e entra em inserção	| nor S ou cc|
| coloca em maiuscula a frase           | nor gUU|
| coloca em minuscula a frase           | nor guu|
+---------------------------------------+-----------+

## EDIÇÂO ##

+---------------------------------------+-----------+
| refaz a edição			            | nor ^r|
| copiar linha				            | nor yy|
| copiar linha atual mais n linhas	    | nor yn|
| copiar n palavras			            | nor ynw|
| cola apos a posicao atual do cursor	| nor p|
| cola antes da posicao atual do cursor	| nor P|
| insere TAB no modo normal		        | nor >>|
| recorta uma linha                     | nor dd|
| recorta n linhas                      | nor ndd|
| recorta palavra atual do cursor	    | nor dw|
| recorta a partir da posição do cursor	| nor D|
| realiza comando em todos os buffers   | com :bufdo "comando" |
+---------------------------------------+-----------+

## MOVIMENTAÇÃO ##

+---------------------------------------+-----------+
| move cursor uma palavra pra frente	| nor w|
| move uma palavra pra tras		        | nor b|
| move cursor para alto da tela		    | nor H|
| move cursor para o final da tela	    | nor L|
| move cursor para final do arquivo	    | nor G|
| move cursor para linha nro x          | nor xG|
| move cursor para inicio arquivo       | nor 1G|
| move cursor para inicio da linha      | nor 0 ou home|
| move cursor 1º caracter nao epaço     | nor ^|
| move cursor final da linha            | nor $|
| move cursor meia tela pra cima        | nor ctrl+u|
| move cursor meia tela pra baixo       | nor ctrl+d|
| move cursor uma sentença pra frente   | nor )|
| move cursor uma sentença pra tras     | nor (|
| move cursor um paragrafo pra frente   | nor }|
| move cursor um paragrafo pra tras     | nor {|
+---------------------------------------+-----------+

## MOVIMENTAÇÃO DE TEXTO ##

+---------------------------------------+-----------+
| move trecho para o fim do texto       | com :X,Ym $|
| move linha para baixo                 | nor ddp|
| move linha para cima                  | nor ddkP|
+---------------------------------------+-----------+

## CONFIGURAÇÔES ##

+---------------------------------------+-----------+
| ativar numero de linhas               | com :set number|
| mudar esquema de cores                | com :set background=light(dark)|
| mudar cor de fundo                    | com :hi Normal ctermbg=black|
+---------------------------------------+-----------+

## VIMBOOK E APRESENTAÇÃO ##

+---------------------------------------+-----------+
| calculadora básica                    | com :echo "conta":w|
| grep interno                          | com :grep termo caminho(pode usar \*\*|
  pra ser recursivo) pipe (para abrir no quickfix)|
| compilar                              | com :make copen|
| editar com comando, avancado          | com :X,Y modo oquefazer (ex: :30,35|
  normal 0>> ou 5,$ normal 0wd3w)|
| autocompletar modo inserção           | ins ^x^n e outras variações |            
| fechar buffer							| com :bd |
  +---------------------------------------+-----------+

## COMANDOS G(Go) ##

+---------------------------------------+-----------+
| mostra doc referenciado no cursor     | nor ga|
| vai para definição de termo           | nor gd|
| vai para definicao global             | nor gD|
+---------------------------------------+-----------+

## REGISTRADORES ##

+---------------------------------------+-----------+
| copia no registrador a                | nor "ayy|
| cola conteudo do registrador a        | nor "ap|
| copia trecho para registrador a       | com :X,Yy a|
+---------------------------------------+-----------+

##  DOBRAS ##

+---------------------------------------+-----------+
| abre/fecha dobra                      | nor za|
| abre dobra recursivamente             | nor zO|
| abre/fecha recursivamente             | nor zA|
| abre todas dobras de um arquivo       | nor zR|
| fecha todas dobras de um arquivo      | nor zM|
+---------------------------------------+------------+

## IDENTAÇÂO ##

+---------------------------------------+-----------+
| identa linha atual                    | nor >> |
| identa linha atual modo inserção      | ins ^t |
| remove identação modo inserção        | ins ^d |
| identa paragrafo atual                | com \>ip |
+--------------------------------------+----------+

## MACROS ##

+---------------------------------------+-----------+
| iniciar macro no registrador a        | nor qa    |
| parar gravacao                        | nor q     |
| executar macro                        | N@a       |
+---------------------------------------+-----------+

## SESSÕES ##

+---------------------------------------+-----------+
| criar um sessão                       | com :mks nomesessao.vim |
| salvar sessao                         | com :mks! nomesessao.vim |
| carregar sessao                       | com :so nomessao.vim |
| carregar sessao fora do vim           | vim -S nomesessao.vim |
| exibir nome e caminho sessao          | com :echo v:this_session |
+---------------------------------------+----------+ 
