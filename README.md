# One of the best linux commands i know

## 📂 Gerenciamento de Arquivos e Diretórios
```sh
man # ver oque o comando faz ex: man ls
touch # criar um arquivo ex: touch arquivo.txt
mkdir -p # cria diretório ex: mkdir -p pasta/subpasta
rm -f # exclui o arquivo/diretório pra sempre ex: rm -f arquivo.txt
trash # ao instalar o pacote "trash" voce pode mandar o arquivo/diretório para a lixeira ex: trash arquivo.txt
cp -r # copiar um arquivo para um diretório ex: cp -r origem/ destino/
mv    # move ou renomeia arquivos/diretórios ex: mv antigo.txt novo.txt
ls -l # Lista arquivos em formato detalhado
find  # busca arquivos/diretórios ex: find /caminho -name "*.txt"
```

## 🔍 Busca e Visualização

```sh
grep # Procura por padrões em arquivos ex: grep "texto" arquivo.txt
cat  # Exbibe o conteudo do arquivo ex: cat arquivo.txt
less # Visualiza arquivos paginados( melhor que `cat` para arquivos grandes) ex: less arquivo.log
head -n # Mostra as primeiras linhas do arquivo ex: tail -n 10 arquivo.log
tail -n # Mostra as ultimas linhas do arquivo
```

## ⚙️ Sistema e Processos

```sh
ps aux # Lista processos em execução ex: ps aux | grep "nginx"
kill   # Encerra um processo ex: kill -9 PID
top    # Monitora processos e uso de recursos ex: htop
htop   # ''''''''
df -h # Mostra espaço em disco ex: df -h
du -sh # Exibe tamanho de um diretório ex: du -sh /pasta/
```

## 🌐 Rede e Internet

```sh
ping # Testa conectividade com um host ex: ping google.com
curl # Baixa arquivos da internet ex: curl -O URL
wget
ssh  # conecta a um servidor remoto ex: ssh user@host
ip a # Mostra informações de rede(substitui ifconfig) ex: ip a
```

## 🛠️ Utilitários Úteis

```sh
chmod # Altera permissões de arquivos ex: chmod +x script.sh 
chown # Altera o dono de um arquivo ex: chown user:group arquivo
tar   # Compacto/descompacta arquivos ex: tar -xzvf arquivo.tar.gz
alias # Cria atalhos para comandos ex: alias ll='ls -la'
```

## 📌 Dicas Extras
- Use `Ctrl + C` para interromper um comando
- Use `Ctrl + R` para buscar no histórico de comandos
- Sempre confira o manual com `man comando` antes de usar flags desconhecidas

## 🔗 Referências Úteis
- [ExplainShell](https://explainshell.com/) - Explica o que cada parte do comando faz.]
- [TLDR Pages](https://tldr.sh/) - Versão simplificada do `man`
