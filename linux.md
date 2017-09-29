### usando o cut ###

-d : delimitador
-c : quais caracteres devem aparecer
-f : qual campo será selecionado

### listando apenas arquivos ###

ls -l | grep -v "^d"

- pwd - mostra pasta atual
- passwd - cria e modifica senhas (precisa ser sudoer)
- whoami - mostra nome do usuario atual
- history - histórico dos comandos

### lidando com conteúdo de arquivo ###

head - mostra as 10 primeiras linhas de um arquivos
tail - mostra as 10 últimas linhas

-n - apresenta a quantidade de linhas

cat - mostra conteúdo arquivos
tac - mostra conteudo dos arquivos, mas ao contrãrio, do fim pro começo

### paginadores ###

less
more

### como fazer um pendrive bootável ###

- primeiro deve-se desmontar o dispositivo:

	umont /dev/sdx

- depois formatar o pendrive: 

	mkfs.vfat **vfat é o tipo de armazenamento, FAT32** /dev/sdx

- por fim, fazer a cópia da mídia para o dispositivo:

	dd if=nomedoarquivoasercopiado.extensao of=/dev/sdx **nao colocar o numero da partição**
