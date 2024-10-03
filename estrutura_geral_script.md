# Estrutura Geral de um Script

Os arquivos de script permitem construir esquemas de execução complexos a partir dos comandos básicos do shell. A forma mais elementar de arquivo de script é apenas um conjunto de comandos em um arquivo texto, com permissões de execução habilitadas. O arquivo `backup.sh`, cujo conteúdo é mostrado a seguir, é um exemplo de script:

```bash
#!/bin/bash
echo "Iniciando backup..."

# montar o diretório do servidor de backup
mount fileserver.ufpr.br:/backup /backup

# efetuar o backup em um arquivo tar compactado
tar czf /backup/home.tar.gz /home

# desmontar o diretório do servidor de backup
umount /backup

echo "Backup concluido!"
