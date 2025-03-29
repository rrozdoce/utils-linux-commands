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

## Extras: Windows 11 commands

### Comandos Úteis no Prompt de Comando (CMD)

```sh
ipconfig # Mostra informações de rede(IP,gateway, DNS, etc.)
ipconfig /release # renovar o ip
ipconfig /renew   # ''''''
ipconfig /flushdns # Limpar o cache DNS
ping # Testa conexão com servidor ou site
tracert # Rastreia a rota que os pacotes fazem até o destino
netstat # Mostra conexões de rede ativas
netstat -ano # Lista todas as conexões com PIDs
tasklist # lista processos em execução
taskkill /im nome_do_processo.exe /if # força o fechamento de um programa
chkdsk # verifica e repara erros no disco ex: chdsk C: /f
sfc /scannow # verifica e repara arquivos corrompidos do sistema
diskpart # ferramenta avançada para gerenciamento de discos(particionamente, formatação)
shutdown /s /t 0 # Desliga o PC imediatamente
shutdown /r /t 0 # Reinicia o PC
shutdown /h      # HIbernação
```

### Comandos do Powershell (Mais forte que o CMD)
```sh
Get-Process # Lista processos em execução
Stop-Process -Name "nome_do_processo" -Force # encerra o processo
Get-NetAdapter # Mostra informações sobre adaptadores de rede
Test-NetConnection # Testa conectividade com um host (similar ao `ping`)
Get-WindowsUpdateLog # Gera um log de atualizações do Windows
Get-Disk             # Mostra informações sobre o disco
Get-Partition        # Mostra informações sobre partições
Set-ExecutionPolicy  # Permite execuções de scripts no Powershell( útil para automação )
```

### Atalhos do Teclado no Windows 11
- `Win + A` → Abre o Centro de Ações.
- `Win + E` → Abre o Explorador de Arquivos.
- `Win + I` → Abre as Configurações do Windows.
- `Win + X` → Menu de contexto avançado (acesso rápido a ferramentas).
- `Win + V` → Histórico da Área de Transferência.
- `Win + Ctrl + D` → Cria uma nova área de trabalho virtual.
- `Win + . ou Win` + ; → Abre o menu de emojis e símbolos.
- `Win + Shift + S` → Ferramenta de captura de tela.
- `Win + Ctrl + Shift + B` → Reinicia o driver de vídeo (útil se a tela travar).

### Ferramentas avançadas Windows 11
- `msconfig` → Configuração do Sistema (inicialização, serviços).
- `devmgmt.msc` → Gerenciador de Dispositivos.
- `diskmgmt.msc` → Gerenciamento de Discos.
- `services.msc` → Serviços do Windows.
- `eventvwr.msc` → Visualizador de Eventos (logs do sistema).
- `gpedit.msc` → Editor de Política de Grupo (disponível apenas em versões Pro/Enterprise).
- `taskmgr` → Gerenciador de Tarefas.
- `control` → Painel de Controle tradicional.

# Gerenciador de pacotes Windows(Winget)
O winget é o gerenciador de pacotes oficial do Windows, introduzido pela Microsoft para facilitar a instalação, atualização e remoção de aplicativos via linha de comando (CMD ou PowerShell). Ele é integrado ao Windows 11 (e também disponível no Windows 10 a partir da versão 1809 com atualizações).
```sh
winget search <pacote> # ex: chrome
winget install <nome_pacote/app> # ex: Google.Chrome/Mozilla.Firefox/Microsoft.VisualStudioCode
winget install --d=<nome_pacote> # id é para especificar o aplicativo exato
# ex:
winget install --id=Notepad++.Notepad++ --version 8.6.2

winget list --name <nome_pacote> # ex: chrome
winget upgrade                   # Lista aplicativos com atualizações disponíveis
winget upgrade --id <nome_pacote> # Atualiza app especifico
winget upgrade --all              # Atualiza todos
winget uninstall <nome_do_app>    # Remove um programa instalado
# ex:
winget uninstall Google.Chrome
winget uninstall --id=Adobe.Acrobat.Reader.64-bit

# Exportar e Importar Lista de Aplicativos
winget export -o apps.json 
winget import -i apps.json

# Mostrar Informações de um App
winget show <nome_do_app>
# ex:
winget show Microsoft.PowerToys

# Limpar Cache do Winget
winget cache clean # Remove arquivos temporários baixados durante instalações.
```

## Vantages de usar Winget
✅ Instalação sem intervenção manual (ótimo para scripts e automação).
✅ Atualiza apps em lote (evita versões desatualizadas).
✅ Integração com repositório oficial da Microsoft (mas também suporta fontes externas).
✅ Mais seguro (evita baixar apps de sites não confiáveis).

## Problemas Comuns e Soluções
❌ "Winget não é reconhecido" → Atualize o Windows ou instale o App Installer na Microsoft Store.
❌ Falha na instalação → Execute o terminal como Administrador ou use --force.
❌ App não encontrado → Verifique o nome exato com winget search.

### Exemplo Prático (Instalar Ferramentas Úteis de Uma Vez)

```sh
winget install Microsoft.PowerToys
winget install Telegram.TelegramDesktop
winget install VideoLAN.VLC
winget install 7zip.7zip
winget install ObsProject.OBSStudio
```
