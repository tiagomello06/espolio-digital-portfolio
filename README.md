<h1 align="center">Espólio Digital</h1>

<p align="center">
  <b>Seu legado digital, protegido e transferido com segurança.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-Servlets_%2B_JSP-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/arquitetura-MVC_%2B_DAO-6D28D9?style=flat-square" alt="MVC">
  <img src="https://img.shields.io/badge/MySQL-banco_relacional-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/segurança-AES_%2B_SHA--256-111827?style=flat-square" alt="AES e SHA-256">
  <img src="https://img.shields.io/badge/projeto-acadêmico_UMC_2025-0EA5E9?style=flat-square" alt="Projeto acadêmico">
</p>

<p align="center">
  <img src="docs/img/03-painel.jpg" alt="Painel do titular" width="900">
</p>

> **Sobre este repositório:** esta é a vitrine do projeto, com descrição, arquitetura e telas.
> O código-fonte é privado. Posso apresentá-lo em entrevista.

---

## O problema

Redes sociais, carteiras de criptomoedas e contas online fazem parte do patrimônio de qualquer pessoa,
mas quase ninguém deixa instruções sobre o que fazer com eles depois da morte. As credenciais se perdem
e os herdeiros ficam sem acesso.

## A solução

Um sistema web em que o **titular** cadastra seus ativos digitais e mensagens póstumas e escolhe **herdeiros**.
Os dados ficam **criptografados e bloqueados**. Para liberar, o herdeiro envia a **certidão de óbito em PDF**,
que passa por análise, e só então recebe o legado.

```mermaid
flowchart LR
    T["Titular"] -->|"cadastra ativos<br/>e herdeiros"| S["Espólio Digital"]
    S --> DB[("MySQL<br/>credenciais criptografadas")]
    H["Herdeiro"] -->|"envia certidão<br/>de óbito (PDF)"| S
    S -->|"análise aprovada"| L["Legado liberado"]
```

## Funcionalidades

- **Cadastro e login** com senha em hash SHA-256 e recuperação por palavra-chave
- **Ativos digitais:** Instagram, Facebook, Twitter, Discord, carteiras cripto (frases-chave) e mensagens póstumas
- **Criptografia AES** das credenciais guardadas no banco
- **Gestão de herdeiros** vinculados por CPF, com aviso quando o herdeiro ainda não tem cadastro
- **Legados recebidos:** o herdeiro vê o que foi deixado para ele, ainda bloqueado
- **Solicitação de liberação** com upload da certidão de óbito em PDF e status de análise
- **Editar perfil** com foto

## Telas

<table>
  <tr>
    <td><img src="docs/img/01-login.jpg" alt="Login"></td>
    <td><img src="docs/img/02-cadastro.jpg" alt="Cadastro"></td>
  </tr>
  <tr>
    <td align="center"><sub>Login</sub></td>
    <td align="center"><sub>Cadastro com aviso de LGPD</sub></td>
  </tr>
  <tr>
    <td><img src="docs/img/04-conectar-conta.jpg" alt="Conectar conta"></td>
    <td><img src="docs/img/05-legados-recebidos.jpg" alt="Legados recebidos"></td>
  </tr>
  <tr>
    <td align="center"><sub>Conectar um ativo e escolher o herdeiro</sub></td>
    <td align="center"><sub>Legados recebidos (bloqueados)</sub></td>
  </tr>
  <tr>
    <td><img src="docs/img/06-certidao-de-obito.jpg" alt="Envio da certidão"></td>
    <td><img src="docs/img/00-mapa-de-navegacao.jpg" alt="Mapa de navegação"></td>
  </tr>
  <tr>
    <td align="center"><sub>Envio da certidão de óbito</sub></td>
    <td align="center"><sub>Mapa de navegação do sistema</sub></td>
  </tr>
</table>

<sub>As telas usam dados de teste.</sub>

## Tecnologias e decisões técnicas

| Camada | Tecnologia |
|---|---|
| Back-end | Java com Servlets, organizado em MVC e camada DAO |
| Front-end | JSP, HTML, CSS e JavaScript |
| Banco de dados | MySQL, com modelagem entidade-relacionamento e script SQL próprio |
| Segurança | Senhas em hash SHA-256 e credenciais criptografadas com AES |
| Ferramentas | NetBeans, Apache Tomcat, Git/GitHub |

## Equipe

Projeto final do curso de Análise e Desenvolvimento de Sistemas da Universidade de Mogi das Cruzes (2025),
feito em grupo com [@diegohenrique-data](https://github.com/diegohenrique-data) e
[@NicolyMartineli](https://github.com/NicolyMartineli).

---

<p align="center">
  <a href="https://www.linkedin.com/in/tiago-mello-duran/">LinkedIn</a> ·
  <a href="https://github.com/tiagomello06">GitHub</a>
</p>
