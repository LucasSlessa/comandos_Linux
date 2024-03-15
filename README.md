# Comandos do Linux, Vim e Servidor

Este documento contém uma lista de comandos úteis do Linux, Vim e alguns comandos de servidor.

## Comandos do Linux:

- `ls`: Mostra os arquivos em um diretório.
- `ll`: Lista todos os diretórios e suas informações.
- `ls -l`: Lista informações de cada arquivo/diretório.
- `ls -l /etc/ssh/sshd_config`: Exibe o arquivo de configuração do servidor SSH.
- `chmod 0-x *`: Remove a permissão de execução de outros em todos os arquivos da pasta.
- `ls -la`: Lista todos os arquivos, incluindo os ocultos.
- `cd`: Navega entre pastas.
- `pwd`: Mostra o caminho do diretório atual.
- `vi <caminho do arquivo>`: Abre o Vim para editar um arquivo.
- `su root`: Troca para o usuário root.
- `journalctl`: Exibe mensagens do registro do sistema.
- `journalctl -x -u named`: Exibe mensagens do registro do sistema para o serviço named.
- `journalctl -xb -u named`: Exibe mensagens detalhadas do registro do sistema para o serviço named.
- `df -h`: Exibe o espaço em disco de forma legível para humanos.
- `passwd`: Permite alterar a senha do usuário atual.
- `sudo <comando>`: Executa um comando com privilégios de superusuário.
- `top`: Exibe informações sobre os processos em execução e a carga do sistema.
- `htop`: Uma versão mais interativa e amigável do comando top.
- `df`: Exibe o espaço em disco disponível em todas as partições.
- `du`: Mostra o uso de espaço em disco de arquivos e diretórios.
- `cat <arquivo>`: Exibe o conteúdo de um arquivo.
- `grep <padrão> <arquivo>`: Procura por um padrão em um arquivo.
- `find <diretório> -name <nome do arquivo>`: Procura por arquivos em um diretório específico. se usarmos `iname` ele ignora uppercases
- `wget <URL>`: Baixa arquivos da internet.
- `tar`: Permite criar, visualizar ou extrair arquivos .tar.
- `zip`/`unzip`: Comprime/descomprime arquivos no formato .zip.
- `ping <host>`: Verifica a conectividade com um host na rede.
- `ssh <usuário>@<host>`: Conecta-se a um host remoto via SSH.
- `scp <arquivo> <usuário>@<host>:<caminho>`: Copia arquivos de/para um servidor remoto via SSH.
- `chmod <permissões> <arquivo>`: Altera as permissões de um arquivo.
- `chown <usuário> <arquivo>`: Altera o proprietário de um arquivo.
- `man <comando>`: Exibe o manual de um comando.
- `id`: Mostra a identificação do usuário e dos grupos.
- `su <User>`: Troca para o usuário desejado.


## Comandos do Vim:

- Navegação com setas.
- `:+<número da linha>`: Vai para a linha desejada.
- `/<texto>`: Procura por um texto no arquivo.
- `esc + q!`: Sai do Vim sem salvar.
- `esc + wq`: Sai do Vim e salva as alterações.
- `i` ou `r`: Entra no modo de edição para editar o conteúdo do arquivo.
-  `:w`: Salva o arquivo.
- `:q`: Sai do Vim.
- `:q!`: Sai do Vim sem salvar as alterações.
- `:wq`: Salva as alterações e sai do Vim.
- `:x`: Salva as alterações e sai do Vim (equivalente a `:wq`).
- `:set number`: Mostra o número de linhas.
- `:set nonumber`: Oculta o número de linhas.
- `:sp <arquivo>`: Abre um novo arquivo na mesma janela, dividindo verticalmente.
- `:vsp <arquivo>`: Abre um novo arquivo na mesma janela, dividindo horizontalmente.
- `Ctrl + w + w`: Alterna entre as janelas divididas.
- `Ctrl + w + q`: Fecha a janela atual.

## Comandos de Servidor:

- `ps aux | grep <usuário>`: Filtra processos por usuário.
- `ps aux | <nome do aplicativo>`: Executa um aplicativo.
- `kill -9 <número do processo>`: Mata um processo.
- `netstat -tulnp`: Mostra as portas TCP e UDP em uso e os programas que as estão utilizando.
- `uptime`: Mostra o tempo de atividade do sistema.
- `whoami`: Mostra o nome do usuário atual.
- `ifconfig`: Mostra informações sobre interfaces de rede.
- `netstat -tulnp`: Mostra as portas TCP e UDP em uso e os programas que as estão utilizando.
- `uptime`: Mostra o tempo de atividade do sistema.
- `who ou w`: Mostra informações sobre os usuários logados no sistema.
- `ps`: Mostra os processos em execução no sistema.
- `kill <PID>`: Mata um processo pelo seu ID de processo.
- `service <nome do serviço> start|stop|restart`: Inicia, para ou reinicia um serviço.
- `systemctl <ação> <nome do serviço>`: Controla serviços no systemd.
- `journalctl`: Exibe mensagens do registro do sistema.
- `cron`: Permite agendar tarefas para serem executadas em momentos específicos.
- `loginctl list-sessions`: Lista as sessões de usuário.
- `loginctl show-session <ID>`: Mostra detalhes sobre uma sessão específica.
- `loginctl show-user <usuário>`: Mostra informações sobre um usuário específico.
- `loginctl show-seat <ID>`: Mostra informações sobre um assento (seat) específico.
- `loginctl show-session <ID> -p Type`: Mostra o tipo da sessão (por exemplo, "tty" para sessões em terminais virtuais).
- `loginctl kill-session <ID>`: Encerra uma sessão de usuário específica.
- `loginctl terminate-user <usuário>`: Encerra todas as sessões de um usuário.
- `loginctl lock-session <ID>`: Bloqueia uma sessão de usuário.
- `loginctl unlock-session <ID>`: Desbloqueia uma sessão de usuário.
- `loginctl enable-linger <usuário>`: Habilita a execução de serviços do usuário em background.
- `loginctl disable-linger <usuário>`: Desabilita a execução de serviços do usuário em background.

## Comandos de DNS:

- `dig <domínio>`: Realiza uma consulta DNS para o domínio especificado.
- `dig <domínio> +short`: Exibe apenas o resultado da consulta DNS de forma resumida.
- `nslookup <domínio>`: Realiza uma consulta DNS para o domínio especificado.
- `host <domínio>`: Realiza uma consulta DNS para o domínio especificado e exibe informações sobre ele.
- `host <endereço IP>`: Realiza uma consulta DNS reversa para o endereço IP especificado.
- `hostname`: Exibe o nome do host local.
- `hostname -f`: Exibe o nome completo do host local (incluindo o domínio).
- `hostname -i`: Exibe o endereço IP do host local.
- `hostname -d`: Exibe o domínio do host local.
- `hostname -f`: Exibe o nome completo do host local
# Comandos de Firewall



## iptables

- `iptables -L`: Lista todas as regras de firewall.
- `iptables -A INPUT -s <IP> -j DROP`: Adiciona uma regra para bloquear pacotes provenientes do IP especificado.
- `iptables -A OUTPUT -d <IP> -j DROP`: Adiciona uma regra para bloquear pacotes destinados ao IP especificado.
- `iptables -A FORWARD -s <IP> -j DROP`: Adiciona uma regra para bloquear pacotes encaminhados do IP especificado.
- `iptables -A INPUT -p <protocolo> --dport <porta> -j ACCEPT`: Adiciona uma regra para permitir tráfego na porta especificada.
- `iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT`: Adiciona uma regra para permitir pacotes relacionados a conexões estabelecidas.

## ip6tables

- `ip6tables -L`: Lista todas as regras de firewall IPv6.
- `ip6tables -A INPUT -s <IP> -j DROP`: Adiciona uma regra para bloquear pacotes IPv6 provenientes do IP especificado.
- `ip6tables -A OUTPUT -d <IP> -j DROP`: Adiciona uma regra para bloquear pacotes IPv6 destinados ao IP especificado.
- `ip6tables -A FORWARD -s <IP> -j DROP`: Adiciona uma regra para bloquear pacotes IPv6 encaminhados do IP especificado.
- `ip6tables -A INPUT -p <protocolo> --dport <porta> -j ACCEPT`: Adiciona uma regra para permitir tráfego IPv6 na porta especificada.
- `ip6tables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT`: Adiciona uma regra para permitir pacotes IPv6 relacionados a conexões estabelecidas.

## ufw (Uncomplicated Firewall)

- `ufw status`: Exibe o status do firewall e as regras configuradas.
- `ufw enable`: Ativa o firewall.
- `ufw disable`: Desativa o firewall.
- `ufw default deny incoming`: Define a política padrão para bloquear todo o tráfego de entrada.
- `ufw default allow outgoing`: Define a política padrão para permitir todo o tráfego de saída.
- `ufw allow <porta>/<protocolo>`: Permite tráfego na porta especificada.
- `ufw deny <porta>/<protocolo>`: Bloqueia tráfego na porta especificada.

## firewalld

- `firewall-cmd --state`: Exibe o estado do firewall.
- `systemctl start firewalld`: Inicia o serviço do firewall.
- `systemctl stop firewalld`: Para o serviço do firewall.
- `firewall-cmd --list-all`: Exibe todas as configurações do firewall.
- `firewall-cmd --zone=public --add-port=<porta>/<protocolo>`: Permite tráfego na porta especificada na zona pública.
- `firewall-cmd --zone=public --remove-port=<porta>/<protocolo>`: Remove permissão de tráfego na porta especificada na zona pública.
- `firewall-cmd --add-service=dns`:permitir trafego de dns se digitarmos `firewall-cmd --permanent --add-service=dns`: permite o dns permanente no firewall.
- `firewall-cmd --reload`:Volta ao ultimo status salvo do firewall.
  
##Extras


- `ss -ltnup` é usado para listar todas as conexões de rede TCP que estão ouvindo em um sistema Linux, juntamente com os processos associados a essas conexões. Aqui está o significado de cada opção do comando:
- `-l`Exibe apenas as conexões que estão escutando (listening).
- `-t` Exibe apenas as conexões TCP.
- `-n` Exibe os números de porta e endereços IP no formato numérico, em vez de resolver nomes.
- `-u` Exibe apenas as conexões UDP.
- `-p` Mostra o processo que está utilizando a conexão.
Em resumo, o comando ss -ltnup mostra todas as conexões TCP que estão escutando, juntamente com os processos associados a essas conexões, 


