# desafio-aws-ec2-dio
Projeto do laboratório AWS EC2 desenvolvido durante a formação da DIO.
# Laboratório AWS EC2 - Gerenciamento de Instâncias

## Descrição

Este repositório foi desenvolvido como entrega do desafio da DIO referente ao laboratório de Gerenciamento de Instâncias EC2 na Amazon Web Services (AWS).

O objetivo é consolidar os conhecimentos obtidos durante as aulas por meio da documentação dos principais conceitos, procedimentos realizados e boas práticas relacionadas ao gerenciamento de instâncias EC2.

---

# Objetivos do Projeto

- Compreender os conceitos fundamentais da Amazon EC2.
- Criar e gerenciar instâncias EC2.
- Configurar grupos de segurança.
- Utilizar chaves SSH.
- Monitorar instâncias.
- Encerrar instâncias de forma segura.
- Documentar todas as etapas realizadas.

---

# O que é Amazon EC2?

O Amazon Elastic Compute Cloud (EC2) é um serviço da AWS que permite criar máquinas virtuais sob demanda na nuvem.

Com ele é possível:

- Hospedar aplicações
- Criar servidores Linux e Windows
- Executar bancos de dados
- Criar ambientes de desenvolvimento
- Escalar aplicações conforme necessidade

---

# Conteúdo aprendido

## 1. Criação de uma instância

Durante o laboratório foram executadas as seguintes etapas:

- Escolha da AMI (Amazon Machine Image)
- Escolha do tipo da instância
- Criação do Key Pair
- Configuração da VPC
- Configuração do Security Group
- Inicialização da instância

---

## 2. Tipos de Instância

Alguns exemplos:

| Tipo | Uso |
|--------|----------------|
| t2.micro | Free Tier |
| t3.micro | Desenvolvimento |
| m5.large | Aplicações Gerais |
| c5.large | Alto processamento |
| r5.large | Memória |

---

## 3. Security Groups

Os Security Groups funcionam como firewall da instância.

Exemplo de regras:

SSH (22)

Origem:
Meu IP

HTTP (80)

Origem:
0.0.0.0/0

HTTPS (443)

Origem:
0.0.0.0/0

---

## 4. Conectando via SSH

Linux

```bash
chmod 400 chave.pem

ssh -i chave.pem ec2-user@IP-PUBLICO
```

Ubuntu

```bash
ssh -i chave.pem ubuntu@IP-PUBLICO
```

---

## 5. Monitoramento

Durante o laboratório foi possível observar:

- CPU
- Memória
- Rede
- Disco
- Status Checks

Utilizando o Amazon CloudWatch.

---

## 6. Encerrando uma instância

Antes de excluir uma instância é importante:

- Realizar backup
- Salvar dados importantes
- Criar uma AMI
- Confirmar que a instância não será mais utilizada

---

# Aprendizados

Durante este laboratório compreendi a importância de:

- Segurança em nuvem
- Gerenciamento correto das instâncias
- Utilização de grupos de segurança
- Custos na AWS
- Monitoramento através do CloudWatch

Também foi possível entender como pequenas configurações podem impactar diretamente na disponibilidade e segurança de um ambiente em nuvem.

---

# Boas práticas

✔ Utilizar somente as portas necessárias

✔ Nunca deixar SSH aberto para qualquer IP

✔ Utilizar Tags

✔ Criar snapshots antes de alterações importantes

✔ Encerrar recursos não utilizados

✔ Utilizar IAM ao invés da conta Root

---

# Estrutura do projeto

```
.
├── README.md
├── docs
├── images
└── scripts
```

---

# Referências

Documentação Oficial AWS

https://docs.aws.amazon.com/ec2/

Amazon EC2 User Guide

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/

GitHub Docs

https://docs.github.com/

Markdown Guide

https://www.markdownguide.org/

---

# Autor

James Vieira

Projeto desenvolvido como requisito para conclusão do laboratório da DIO.
