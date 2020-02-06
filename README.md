# Prompt-Dos
Senha-e-Ocultar-Pasta

1- crie uma nova pasta (nome a sua escolha)
-------------------------------------------------------------------------------

2- dentro desta pasta crie um arquivo com o bloco de notas e dentro do arquivo cole isto
-------------------------------------------------------------------------------
 CLS

 @ECHO OFF
 
 title Folder Private
 
 if EXIST "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" goto
 UNLOCK
 
 if NOT EXIST Private goto MDLOCKER
 :CONFIRM
 
 echo Are you sure you want to lock the folder(Y/N)
 
 set/p "cho=>"
 
 if %cho%==Y goto LOCK 
 
 if %cho%==y goto LOCK
 
 if %cho%==n goto END
 
 if %cho%==N goto END
 
 goto CONFIRM
 
 :LOCK
 
 ren Private "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
 
 attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
 
 echo Folder locked
 
 goto End
 
 :UNLOCK
 
 echo Enter password to unlock folder
 
 set/p "pass=>"
 
 if NOT %pass%== password here goto FAIL
 
 attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
 
 ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" Private
 
 echo Folder Unlocked successfully
 
 goto End
 
 :FAIL
 
 echo Invalid password
 
 goto end
 
 :MDLOCKER
 
 md Private
 
 echo Private created successfully
 
 goto End
 
 :End
-------------------------------------------------------------------------------

 3- depois de copiar os comandos acima para dentro do bloco de notas
 Na linha 23 você encontrara esta frase: “ password here” mude isto para a sua senha que deseja
-------------------------------------------------------------------------------

 4- depois de colocar sua senha salve o arquivo com um nome de sua escolha
 E coloque nele a extensão .bat
 EX: locker.bat
-------------------------------------------------------------------------------

 5- agora na sua pasta você tera um arquivo bat com o nome q você colocou
-------------------------------------------------------------------------------

 6- abra ele e automaticamente criara uma pasta chamada Private
-------------------------------------------------------------------------------

 7- coloque o que você quiser dentro da pasta Private e para esconder esta pasta Abra o arquivo bat e na tela de prompt de comando coloque Y
 Isso fará com que a pasta Private seja escondida
-------------------------------------------------------------------------------

 8- para poder abrir sua pasta Private abra o arquivo bat que criamos e coloque sua senha no prompt de commando

 Pronto sua pasta aparecera