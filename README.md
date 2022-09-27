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


|Data Set Names | Espaço | Descrição |
| --- | --- | --- |
| UNV.AUNVLOAD | 6500 | Biblioteca de distribuição SMP/E para a biblioteca de carga de produtos.|
| UNV.AUNVNLS | 30 | Biblioteca de distribuição SMP/E para a biblioteca de apoio linguístico nacional do produto.|
| UNV.AUNVSAMP | 30 | Biblioteca de distribuição SMP/E para a biblioteca de amostras de produtos.|
| UNV.AUNVTMPL | 	60 | Biblioteca de distribuição SMP/E para arquivos de modelos de configuração.|
| UNV.SMP.CSI | n/a | Cluster SMP/E CSI VSAM para zonas SMP/E de Agente Universal.|
| UNV.SMP.CSI.DATA | 75 | Dados SMP/E CSI VSAM para zonas SMP/E de Agente Universal.|
| UNV.SMP.CSI.INDEX | 15 | Índice SMP/E CSI VSAM para zonas SMP/E de Agente Universal.|
| UNV.SMP.SMPLOG | 30 | Arquivo de log SMP/E.|
| UNV.SMP.SMPLOGA | 30 | Arquivo de backup SMP/E.|
| UNV.SMP.SMPLTS | 100 | Biblioteca de destino SMP/E para versões básicas de módulos de carga usando uma alocação SYSLIB.|
| UNV.SMP.SMPMTS | 30 | SMP/E biblioteca alvo para macros existentes apenas nas bibliotecas de distribuição.|
| UNV.SMP.SMPPTS | 4500 | Armazenamento temporário do SMP/E SYSMOD.|
| UNV.SMP.SMPSCDS | 30 | Biblioteca de backup de zona SMP/E.|
| UNV.SMP.SMPSTS | 30 | SMP/E biblioteca alvo para fonte existente apenas nas bibliotecas de distribuição.|
| UNV.SUNVLOAD | 6500 | SMP/E biblioteca alvo para a biblioteca de carga de produtos.|
| UNV.SUNVNLS | 30 | SMP/E biblioteca alvo para a biblioteca de suporte ao idioma nacional do produto.|
| UNV.SUNVSAMP | 30 | Biblioteca SMP/E para a biblioteca de amostras de produtos.|
| UNV.SUNVTMPL | 60 | SMP/E biblioteca alvo para arquivo de modelo de configuração.|

## Non-SMP/E Data Sets

A tabela a seguir lista os data sets non-SMP/E - e suas necessidades de espaço - que são alocados e catalogados como parte do Agente Universal para instalação do pacote z/OS.

Dependendo de suas escolhas de instalação, os qualificadores de alto nível do data sets podem ser diferentes.

|Data Set Names | Espaço | Descrição |
| --- | --- | --- |
| UNV.MDL | 1 | Modelo de alocação de data set sequenciais.|
| UNV.UAG| 1 | Modelo de alocação do data set de registro do Agente do Centro de Automação Universal.|
| UNV.UAG.AGENT.LOG | n/a | Data set de registro de Agente do Centro de Automação Universal GDG base.|
| UNV.UCRDB | 	15 | Banco de dados de certificados universais.|
| UNV.UECDB | 4500 | Controlador Empresarial Universal HFS ou banco de dados zFS.|
| UNV.UNVCOMP | 15 | Biblioteca de definição de componentes do Agente Universal.|
| UNV.UNVCONF | 15 | Biblioteca de configuração do Agente Universal. |
| UNV.UNVCREF | 75 | Biblioteca de referência de comandos do Universal Command Server. |
| UNV.UNVDB | 150 | Corretor Universal HFS ou banco de dados zFS. |
| UNV.UNVJSC | n/a  | VSAM Job Submission Checkpoint (JSC) cluster. |
| UNV.UNVKSTR | 75 | Data set da Universal Broker Key Store. |
| UNV.UNVSPOOL | 3000 | Agente universal HFS ou banco de dados de spool zFS. |
| UNV.UNVTRACE | 150 | Data set de rastreamento PDS/E da Universal Broker. |
| UNV.V6R4M0.INSTALL |30 | Instalação e manutenção do pacote de Agentes Universais JCL. |

## Suporte de Plataforma para Controlador Universal 7.2.x e Agente Universal 7.2.x

Esta página fornece informações de suporte de plataforma para os seguintes produtos do Centro de Automação Universal:

- Universal Controller 7.2.x
- Universal Agent 7.2.x
  - Universal Command
  - Universal Data Mover
  
  
|Plataforma | Supported Realeases |Universal Controller |Universal Agent| USAP |UPPS |SOA Agent |UDM | UEC| UEC Clients |Notes
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| IBM z/OS | 2.2, 2.3, or 2.4 |  | - [x] | OK |  |  | OK | OK |  | * A OMS não está disponível.|
