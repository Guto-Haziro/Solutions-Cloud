# Golden Image

![alt text](goldenimage.png)

## Objetivo
A solução do GoldenImage traz agilidade, resiliencia e segurança para ambientes containerizados no ECS. Esta solução visa implementar as imagens de maneira automatizada assim que a imagem é adicionada no repositório, acionado por uma pipeline que adiciona a imagem no bucket (utilizado de repositório dentro da AWS) e que ativa o Image Builder através do EventBridge e realiza a atualização do launch template, cria uma nova AMI e atualiza o container. A solução também conta com a recuperação imediata do ambiente caso qualquer erro aconteça no momento do Deploy da aplicação. Caso o container não consgia subir, ele registra o log no Cloudwatch e realiza o refresh imediato voltando para o launch template anterior e realizando o rollback on ECS.

_**Baixe o diagrama .drawio para ter uma visão detalhada da arquitetura**_