## SB-Setup-z-OS
Documentação Stonebranch Setup z/OS. 


## Instalação z/OS - Requisitos de instalação

O Agente Universal para z/OS requer as seguintes versões de software:

- z/OS 2.2, 2.3, or 2.4.
- SMP/E 3.5 or later.
- IBM Communication Server for z/OS 2.2, 2.3, or 2.4.
- IBM Language Environment (LE) for z/OS 2.2, 2.3, or 2.4.
- Workstation capable of establishing a TCP/IP network connection to the z/OS system.
- TSO user ID with an OMVS segment.
- About 1900 cylinders of DASD.
- Two available TCP/IP ports on z/OS.

Todos os programas de Agente Universal utilizam os Serviços de Sistema z/OS UNIX. Como tal, o z/OS UNIX requer o perfil do usuário com o qual um programa executa para ter um segmento OMVS devidamente definido. O segmento OMVS deve definir um valor UID único. O valor HOME deve especificar um diretório home existente ao qual o ID do usuário tem acesso de leitura e escrita.

Além disso, o(s) grupo(s) ao(s) qual(is) o ID do usuário está associado(s) deve(m) ter um segmento OMVS que defina um valor GID único para o grupo. Consulte o manual de Planejamento de Serviços de Sistema UNIX da IBM para obter detalhes adicionais sobre a definição de usuários z/OS UNIX.

## Requisitos de espaço para o conjunto de dados

Como parte do Agente Universal para instalação do pacote z/OS, vários conjuntos de dados SMP/E e não-SMP/E são alocados e catalogados. Os requisitos de espaço para estes conjuntos de dados estão listados em Instalação z/OS - Data Set Inventory.

## Requisitos da plataforma

Como os requisitos da plataforma podem mudar com novos lançamentos de um produto, consulte a página Suporte de Plataforma para o Controlador Universal 7.2.x e Agente Universal 7.2.x para certificar-se de que sua plataforma seja suportada antes de realizar uma instalação.

## Instalação z/OS - Data Set Inventory

- Tipos de Data Sets
- SMP/E Data Sets 
- Non-SMP/E Data Sets

## Tipos de Data Sets

Como parte do Agente Universal para instalação do pacote z/OS, dois tipos de data sets são alocados e catalogados:

- SMP/E data sets
- Non-SMP/E data sets

## SMP/E Data Sets

A tabela a seguir lista os data set SMP/E - e suas necessidades de espaço - que são alocados e catalogados como parte do Agente Universal para instalação z/OS.

Dependendo de suas escolhas de instalação, os qualificadores de alto nível do data set podem ser diferentes.


| Data Set Names | Espaço | Descrição |
| --- | --- | --- |
| UNV.AUNVLOAD | 6500 | Biblioteca de distribuição SMP/E para a biblioteca de carga de produtos.|
