<?php
	$digito = filter_input(INPUT_GET,'Input');
	IF(isset($_GET ['confirmar']) == 'confirmar'){
	$arquivo = "urna.txt";
	$conteudo = ",".$digito;
	$abertura = fopen("$arquivo","a+");
	$gravaçao = fwrite($abertura,$conteudo);
	#Reposiciona o ponteiro no inicio do arquivo
	fseek($abertura,0);
	$leitura = fread($abertura,filesize($arquivo));
	fclose($abertura);
}
	$contbranco=0;
    $arquivo= "branco.txt";
    $conteudo2=$contbranco++;
    $abertura=fopen("$arquivo","a+");
    $gravacao=fwrite($abertura,$conteudo);
    #Reposiciona o ponteiro no início do arquivo
    fseek($abertura,0);
    $leitura=fread($abertura,filesize($arquivo));
    fclose($abertura);
?>

<!DOCTYPE html>
<html>
<head>
<title>urna</title>
</head>
	<body>
		<center>
			
				<FORM NAME="ur"  method="get" action="urna.php">
		    

				    <legend> Urna </legend>
			<tr>
						<td ALIGN="CENTER">
					<INPUT TYPE="text"  NAME="Input" SIZE="20"><br/>
						</td>
			</tr>
			<tr>
					<td><input type="button" NAME="one" value="1" onClick="ur.Input.value += '1'"/>
					<input type="button" value="2" onClick="ur.Input.value += '2'"/>		
					<input type="button" value="3" onClick="ur.Input.value += '3'"/></br>
					</td>
			</tr>
			<tr>
					<td><input type="button" value="4" onClick="ur.Input.value += '4'"/>
					<input type="button" value="5" onClick="ur.Input.value += '5'"/>	
					<input type="button" value="6" onClick="ur.Input.value += '6'"/></br>
					</td>
			</tr>
			<tr>
					<td><input type="button" value="7" onClick="ur.Input.value += '7'"/>
					<input type="button" value="8" onClick="ur.Input.value += '8'"/>		
					<input type="button" value="9" onClick="ur.Input.value += '9'"/></br></td>
			</tr>
			<tr>
					  
					<td ALIGN="CENTER"><input type="button" value="0" onClick="ur.Input.value += '0'"/></br></td>
						
			</tr>
			<tr>
					<td><input type="submit" value="branco" onClick="ur.input.value += ''">
<input type="submit" value="confirmar" name="confirmar"/>
<input type="reset" value="resetar"/>
</tr></td>
       
				</table></br>
	
</TABLE>
</FORM>
</CENTER>
</html>
