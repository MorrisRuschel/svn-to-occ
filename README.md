# svn-to-occ
Script desenvolvido para publicar no ambiente de testes e produção diretamente após salvar os arquivos no versionamento.

# Requisitos
- TortoiseSVN
- PHP
- Plataforma Oracle Commerce Cloud

# Passo a passo
Instalar o tortoiseSVN com opção de command line ativa.
Colocar os arquivos do PHP no c:\php\php.exe
Os logs de cada usuário (individual) ficam salvos em c:\wcAutoPublish\logs\
O arquivo de configuração fica em c:\wcAutoPublish\config.php

# Adicionando Hook ao repositório
- Adicionar o Hook no repositório:
- Clicar com o botão direito -> TortoiseSVN -> Settings -> Hook Scripts -> Add ->
- Hook Type: Post-Commit Hook
- Working Copy Path: c:\projetos\widgets
- Command Line To Execute: c:\wcAutoPublish\libs\php\php.exe C:\wcAutoPublish\test.php
- Wait for the script to finish: Check
- Always execute the script: Check
- -> OK

