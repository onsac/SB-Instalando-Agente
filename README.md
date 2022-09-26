## SB-Setup-z-OS
Documentação Stonebranch Setup z/OS. 


## Requisitos do sistema

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

## Instalação z/OS - Requisitos de instalação
