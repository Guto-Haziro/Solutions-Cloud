# Webapp

## Objetivo

### Este projeto conta com 3 fases, visando automação nas criações e atualizações do ambiente.

* A **Fase 1** conta com a criação da infraestrutura na qual usa uma aplicação hospedada em EC2 com alta disponibilidade  que utiliza RDS e S3 para upload de midia e ciração de cadastros, com atualizações automatizadas com o CodePipeline e o CodeDeploy

* A **Fase 2** foi o plano de automatizar a criação de infraestruturas futuras com IaC utilizando Terraform e Cloudformation, assim para proximas aplicações a infraestrutura será criada de forma mais agil e padronizada conforme necessário.

* A **Fase 3** está voltada para a segurança da aplicação, fechando as rotas de rede para banco de dados e S3, e liberando apenas acessos https. Também foi implementado camadas de segurança na chegada do load balancer, sendo acrecentados um DNS com certiicado valido, cloudfront para melhor experiencia do cliente e proteção a ataques DDOS, e reforço da solução Lambda@Edge para ataques comuns como Strict-Transport-Security, Content-Security-Policy, X-Content-Type-Options, X-Frame-Options, and X-XSS-Protection.