# Desafio4_code_girls

## Implementando Infraestrutura Automatizada com AWS CloudFormation

Este repositório contém minhas anotações, aprendizados e insights sobre a experiência de implementar uma infraestrutura automatizada utilizando o AWS CloudFormation.
O objetivo desta prática foi compreender como o CloudFormation permite provisionar e gerenciar recursos da AWS de forma automatizada e consistente, transformando código em infraestrutura — o famoso conceito de IaC (Infrastructure as Code).

## O que é o AWS CloudFormation

O AWS CloudFormation é um serviço que automatiza a criação, configuração e atualização de recursos na nuvem AWS a partir de templates declarativos, escritos em YAML ou JSON.
Com ele, é possível definir tudo o que compõe uma infraestrutura — como instâncias EC2, buckets S3, VPCs, Security Groups, entre outros — de forma versionável e reproduzível.

Principais vantagens:

- Automação completa do provisionamento;
- Padrões reutilizáveis de infraestrutura;
- Integração com outros serviços da AWS (CodePipeline, CloudWatch, IAM, etc.);
- Controle de versões e rollback automático em caso de erro.

## Experiência Prática

Durante a prática, implementei uma infraestrutura simples, composta por:

Uma VPC com sub-redes públicas e privadas;

Uma instância EC2 para hospedagem de aplicação;

Um bucket S3 para armazenamento de arquivos;

Security Groups configurando o tráfego de entrada/saída.

O template foi desenvolvido em YAML e testado diretamente pelo console da AWS, simulando um fluxo real de deploy automatizado.


## Passos seguidos:

Criação do template infra.yaml;

Validação sintática do arquivo pelo CloudFormation Designer;

Deploy do stack via AWS Console;

Verificação da criação automática dos recursos;

Ajustes e reimplantação do stack para observar a atualização incremental.


## Insights e Aprendizados

Durante a atividade, percebi que:

Infraestrutura como código reduz erros humanos e garante padronização entre ambientes (dev, test, prod).

O CloudFormation é altamente declarativo: não é preciso se preocupar com a ordem de criação dos recursos — ele entende as dependências automaticamente.

O rollback automático é essencial: se algo falha, o serviço reverte todas as alterações, evitando ambientes inconsistentes.

Pequenas alterações exigem atenção, pois o reprocessamento do stack pode recriar recursos (impactando IPs, dados, etc.).

O uso de Parameters, Outputs e Mappings traz flexibilidade e evita duplicação de código.

## Conclusão

Implementar infraestrutura automatizada com o AWS CloudFormation foi uma experiência que reforçou a importância de automação, versionamento e controle em ambientes de nuvem.
Percebi como o IaC facilita a colaboração entre equipes, a reprodutibilidade dos ambientes e a escalabilidade das operações.
