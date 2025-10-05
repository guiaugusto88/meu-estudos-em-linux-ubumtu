# Meus Estudos em Linux (Ubuntu)

Bem-vindo ao meu repositório de anotações sobre Linux!

Este é um projeto pessoal para documentar meu aprendizado de comandos, scripts e conceitos do sistema operacional Linux, com foco na distribuição Ubuntu.

## Estrutura de Diretórios Essenciais do Linux

* `**/bin**`: Armazenamento de arquivos binários essenciais do sistema.
* `**/boot**`: Armazenamento de arquivos necessários para a inicialização do sistema, incluindo o carregador de inicialização (boot loader) e o kernel do Linux.
* `**/dev**`: Armazenamento de arquivos de dispositivo (device files) que representam dispositivos de hardware, como discos rígidos, terminais e outros periféricos.
* `**/etc**`: Armazenamento de arquivos de configuração do sistema.
* `**/home**`: Armazenamento de diretórios pessoais dos usuários.
* `**/lib**`: Armazenamento de bibliotecas compartilhadas essenciais para binários localizados nos diretórios `/bin` e `/sbin`.
* `**/media**`: Ponto de montagem para mídias removíveis (drivers USB, por exemplo).
* `**/mnt**`: Ponto de montagem temporária para sistemas de arquivos. Usado para montar temporariamente outros sistemas de arquivos durante a administração do sistema.
* `**/opt**`: Armazenamento de aplicativos opcionais e pacotes de software adicionais que não fazem parte da instalação padrão do sistema.
* `**/proc**`: Sistema de arquivos virtual que armazena informações sobre os processos em execução e o estado do kernel.
* `**/root**`: Diretório pessoal do usuário root (superusuário).
* `**/run**`: Armazenamento de informações voláteis sobre o sistema desde a última inicialização, como PID files e sockets.
* `**/sbin**`: Armazenamento de binários essenciais para a administração do sistema, necessários para o boot e recuperação do sistema.
* `**/srv**`: Armazenamento de dados específicos de serviços fornecidos pelo sistema.
* `**/sys**`: Sistema de arquivos virtual que fornece informações e interfaces para o kernel do Linux.
* `**/tmp**`: Armazenamento de arquivos temporários criados por aplicativos e pelo sistema. Esses arquivos geralmente são excluídos ao reiniciar o sistema.
* `**/usr**`: Armazenamento de dados de usuário mais instalados pelo sistema, incluindo binários adicionais, bibliotecas e arquivos de cabeçalho.
* `**/var**`: Armazenamento de arquivos variáveis, como logs, filas de email e arquivos de spool.


## Mais Comandos Úteis

### `pwd` (Print Working Directory)
Exibe o caminho completo do diretório atual em que você está no terminal. É o seu "onde estou?".

### `ls` (List)
Lista os arquivos e diretórios no diretório atual.
* **Opção `-a`**: Exibe também arquivos ocultos (que começam com `.`).

### `cd` (Change Directory)
Altera o diretório atual para o especificado.
* **Exemplo**:
  ```bash
  # Muda para o diretório "projeto" (se ele existir a partir de onde você está)
  cd projeto
  ```

### `sudo` (SuperUser Do)
Permite a execução de um único comando com privilégios de superusuário (root), que é o administrador máximo do sistema.
* **Exemplo**:
  ```bash
  # Tenta listar o conteúdo do diretório /root, que normalmente é restrito.
  sudo ls /root
  ```

### `sudo -i` e `sudo su`
Ambos os comandos iniciam uma sessão de shell interativa como o superusuário (root), eliminando a necessidade de digitar `sudo` antes de cada comando.
* `sudo -i`: Inicia uma sessão como root, mas carrega o ambiente e as configurações do próprio root. É considerado mais seguro e limpo.
* `sudo su`: Também se torna root, mas tende a manter mais variáveis de ambiente do seu usuário original.

> **Atenção**: Use sessões de root (`sudo -i` ou `sudo su`) com extremo cuidado. Com grandes poderes vêm grandes responsabilidades! Um comando errado como root pode danificar o sistema.

### `cat` (Concatenate)
Exibe o conteúdo de um ou mais arquivos de texto diretamente no terminal.
* **Exemplo**:
  ```bash
  # Exibe o conteúdo do arquivo de configuração do sistema "fstab"
  cat /etc/fstab
  ```

### `exit`
Encerra a sessão atual do shell. Se você estiver em uma sessão de root (`sudo -i`), o `exit` te retornará ao seu usuário normal. Se estiver no seu usuário normal, ele fechará o terminal.

### `git clone`
Cria uma cópia (um "clone") local de um repositório Git que está em um servidor remoto (como o GitHub).
* **Exemplo**:
  ```bash
  # Clona o repositório do projeto Adopet para uma pasta local
  git clone [https://github.com/alura-cursos/adopet-frontend-cypress](https://github.com/alura-cursos/adopet-frontend-cypress)
  ```
