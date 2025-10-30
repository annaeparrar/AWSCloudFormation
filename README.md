# Desafio DIO: Implementando Infraestrutura Automatizada com AWS CloudFormation


## Objetivo

Este repositório documenta a implementação de uma infraestrutura automatizada na AWS utilizando o serviço **CloudFormation**. O objetivo principal é demonstrar a aplicação prática dos conceitos aprendidos e servir como material de apoio (Anotações e Insights) para estudos futuros.

---

## Conceitos Chave de CloudFormation

Aqui estão os conceitos fundamentais que foram explorados durante a prática:

* **Template (Modelo):** Arquivo (YAML ou JSON) que descreve os recursos da AWS que desejamos provisionar. É o "código" da nossa infraestrutura.
* **Stack (Pilha):** É a unidade de gerenciamento no CloudFormation. Representa a coleção de recursos da AWS que são criados e gerenciados como uma única unidade a partir de um template.
* **Resources (Recursos):** A seção essencial do template, onde definimos os serviços da AWS que serão criados (e.g., `AWS::EC2::VPC`, `AWS::S3::Bucket`).
* **Parameters (Parâmetros):** Permite a entrada de valores personalizados no momento da criação da *Stack*, tornando o template reutilizável (e.g., nome do ambiente, tipo de instância EC2).
* **Outputs (Saídas):** Valores que podem ser retornados pela *Stack* após sua criação, úteis para referenciar recursos em outras *Stacks* ou para uso externo.

---

## Detalhes da Infraestrutura Implementada

Neste desafio, foi implementada a seguinte infraestrutura (descreva o que seu template faz):

1.  **Recurso Principal:** Criação de uma **Virtual Private Cloud (VPC)** na AWS.
2.  **Tecnologia:** AWS CloudFormation.
3.  **Linguagem do Template:** YAML.

---

## Passos para Implementar a Stack

Para recriar esta infraestrutura em sua conta AWS, siga os seguintes passos:

1.  **Acesso:** Faça login no console da AWS.
2.  **Serviço:** Navegue até o serviço **CloudFormation**.
3.  **Criação:** Clique em "Criar Stack" (`Create stack`).
4.  **Template:** Selecione "Carregar um arquivo de modelo".
5.  **Detalhes:**
    * Forneça um nome para a Stack.
    * Preencha os **Parâmetros** solicitados.
6.  **Revisão:** Confirme e aceite as capacidades necessárias.
7.  **Criação:** Clique em "Criar Stack" (`Create stack`) e aguarde até que o *status* mude para `CREATE_COMPLETE`.

---

## Insights e Aprendizados

Esta é a seção mais importante para demonstrar sua compreensão. **Compartilhe seus aprendizados!**

### Lições Aprendidas

* **Dependência de Recursos:** Entendi como o CloudFormation gerencia as dependências. Por exemplo, a Subnet só pode ser criada após a VPC estar completamente provisionada.
* **Rollback e Erros:** Observei que, em caso de erro na criação de um recurso, o CloudFormation executa automaticamente um *rollback*, tentando reverter a infraestrutura para o estado anterior, o que é crucial para manter a consistência.
* **Reutilização com Parâmetros:** A seção `Parameters` permite que o mesmo código seja usado em diferentes ambientes (Desenvolvimento, Teste, Produção) apenas alterando os valores de entrada, o que torna o IaC (Infrastructure as Code) eficiente.

### Desafios Encontrados e Soluções

* **Desafio:** Inicialmente, tive um erro de sintaxe YAML, usando espaços em vez de tabulações em um bloco específico.
* **Solução:** Utilize ferramentas de validação de YAML online para garantir que o template esteja bem formatado antes de fazer o *upload* na AWS. O validador do CloudFormation (Check Template) também é fundamental.

---
