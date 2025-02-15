# AWS IAM Key Rotation

![alt text](rotatekey.png)

## Objetivo

#### Esta solução é altamente recomendada nos casos de uso de API Keys do IAM em aplicações de comunicação com a AWS, fornecendo método de segurança de dois fatores e totalmente automatizado, podendo ser utilizado em ambientes multi-account.

Desenvolvi modelos do CloudFormation e scripts Python que configurará uma função de auto-rotação que rotacionará automaticamente suas chaves de acesso do usuário do AWS IAM a cada 90 dias. Em 100 dias, ele desabilitará as chaves de acesso antigas. E, finalmente, em 110 dias, ele excluirá as chaves de acesso antigas. Ele também configurará um segredo dentro do AWS Secrets Manager para armazenar as novas chaves de acesso, com uma política de recursos que permite apenas o acesso do usuário do AWS IAM a elas. Há também automação para enviar e-mails com um modelo de e-mail personalizado via SES que alertará os proprietários da conta quando ocorrer a rotação.

_**Baixe o diagrama .drawio para ter uma visão detalhada da arquitetura**_