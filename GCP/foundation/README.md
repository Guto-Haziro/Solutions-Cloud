# Foundation GCP

## Objetivo
O objetivo é proporcionar uma base sólida e confiável na GCP, garantindo um ambiente que atenda aos requisitos de segurança, performance e escalabilidade.

Para este projeto, foi pensado na padornização de um Foundation GCP para utilização futura dos workloads principais. Inicialmente o maior foco era voltado para uma GCP responsável pelo DR do ambiente kubernetes no on-premisses, e para isso seria necessário um projeto envolvendo a solução de uma VPC Shared para conexão de recursos on-premisses e cloud abrangendo projetos com workloads distintos, sendo cada um, uma jornada da aplicação. 

O provedor também será utilizado para armazenamento de backups de todos os workloads que rodam na cloud e no on-premisses.

## Soluções
* Identity Center com Workspace G-suite
* Tag para indentificação de recursos, projetos e ambientes
* Projeto VPC Shared
* Projeto Storage
* Segregação de pastas Workloads, VPC e Storage