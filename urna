<?php
#teste_arquivo.php
$arquivo = "urna.txt";
$conteudo = "Isto é um teste";
$abertura = fopen("$arquivo","a+");
$gravaçao = fwrite($abertura,$conteudo);
echo "Número de caracteres gravados: $gravacao";
#Reposiciona o ponteiro no inicio do arquivo tseek($abertura,0);
$leitura = fread($abertura,filesize($arquivo));
fclose($abertura);
echo "<br>Conteúdo do arquivo: $leitura";
?>
