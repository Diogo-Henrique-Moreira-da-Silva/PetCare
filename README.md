# 🐾 PetCar

> Sistema web para facilitar a adoção responsável de animais, conectando adotantes a ONGs, abrigos e protetores independentes.

---

## 🚧 Status do Projeto

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-green?style=for-the-badge)
![Versão](https://img.shields.io/badge/vers%C3%A3o-1.0-blue?style=for-the-badge)
![UML](https://img.shields.io/badge/UML-PlantUML-orange?style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791?style=for-the-badge\&logo=postgresql\&logoColor=white)
![Projeto Acadêmico](https://img.shields.io/badge/Projeto-Acad%C3%AAmico-purple?style=for-the-badge)

---

## 📚 Índice

* [Sobre o Projeto](#-sobre-o-projeto)
* [Funcionalidades Principais](#-funcionalidades-principais)
* [Atores do Sistema](#-atores-do-sistema)
* [Histórias de Usuário](#-histórias-de-usuário)
* [Arquitetura](#-arquitetura)
* [Diagramas do Projeto](#-diagramas-do-projeto)
* [Modelo de Dados](#-modelo-de-dados)
* [Estrutura de Pastas](#-estrutura-de-pastas)
* [Histórico de Revisões](#-histórico-de-revisões)
* [Autores](#-autores)
* [Licença](#-licença)

---

## 📝 Sobre o Projeto

O **PetCar** é um sistema web voltado para a adoção responsável de animais. A plataforma tem como objetivo aproximar pessoas interessadas em adotar animais de ONGs, abrigos e protetores independentes que possuem animais disponíveis para adoção.

Por meio do sistema, a ONG pode cadastrar animais, editar suas informações, acompanhar solicitações de adoção e conversar com possíveis adotantes. O adotante pode visualizar animais disponíveis, aplicar filtros de busca, consultar a ficha completa do animal, verificar a localização aproximada do anúncio, solicitar adoção e acompanhar o andamento do processo.

O projeto também prevê integração com uma **API externa de mapas/localização**, permitindo que o adotante visualize a distância aproximada entre sua localização e o local onde o animal está anunciado.

Este projeto foi desenvolvido como parte da disciplina **Projeto de Software**, com foco na documentação de requisitos, casos de uso, arquitetura, diagramas UML e modelo de dados.

---

## ✨ Funcionalidades Principais

* Cadastro e login de usuários;
* Cadastro de animais para adoção;
* Edição dos dados dos animais cadastrados;
* Listagem de animais disponíveis;
* Filtro por espécie, porte, idade e localização;
* Visualização da ficha completa do animal;
* Visualização da distância aproximada entre adotante e animal;
* Visualização da localização aproximada do animal em mapa;
* Solicitação de adoção;
* Análise da solicitação pela ONG;
* Alteração do status da adoção;
* Notificação ao adotante e à ONG;
* Histórico de solicitações;
* Chat entre adotante e ONG.

---

## 👥 Atores do Sistema

### Adotante

Usuário interessado em procurar animais disponíveis para adoção. O adotante pode visualizar animais, aplicar filtros, consultar fichas, verificar localização, solicitar adoção, acompanhar o histórico de solicitações e conversar com a ONG pelo chat.

### ONG/Abrigo/Protetor

Usuário responsável pelo cadastro dos animais disponíveis para adoção. Pode cadastrar e editar animais, analisar solicitações recebidas, alterar o status da adoção, acompanhar históricos e responder mensagens dos adotantes.

---

## 📌 Histórias de Usuário

| ID   | História de Usuário                                                                                                                                                |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| HU01 | Como adotante, quero me cadastrar na plataforma, para poder procurar animais disponíveis para adoção.                                                              |
| HU02 | Como usuário, quero realizar login na plataforma, para acessar as funcionalidades do sistema.                                                                      |
| HU03 | Como ONG, quero cadastrar animais para adoção, para que adotantes possam visualizar os animais disponíveis.                                                        |
| HU04 | Como ONG, quero editar os dados dos animais cadastrados, para manter as informações sempre atualizadas.                                                            |
| HU05 | Como adotante, quero visualizar a lista de animais disponíveis, para escolher um animal que tenha interesse em adotar.                                             |
| HU06 | Como adotante, quero filtrar animais por espécie, porte, idade e localização, para encontrar animais compatíveis com minha preferência.                            |
| HU07 | Como adotante, quero visualizar a ficha completa do animal, para conhecer suas características antes de solicitar a adoção.                                        |
| HU08 | Como adotante, quero solicitar a adoção de um animal, para que a ONG responsável possa analisar meu pedido.                                                        |
| HU09 | Como ONG, quero analisar as solicitações de adoção recebidas, para aprovar ou recusar os pedidos dos adotantes.                                                    |
| HU10 | Como ONG, quero alterar o status da adoção, para manter o processo atualizado no sistema.                                                                          |
| HU11 | Como adotante, quero receber notificações sobre minha solicitação de adoção, para acompanhar o andamento do processo.                                              |
| HU12 | Como adotante, quero consultar meu histórico de solicitações, para acompanhar os pedidos de adoção que já realizei.                                                |
| HU13 | Como ONG, quero consultar o histórico de solicitações recebidas, para acompanhar os processos de adoção dos animais cadastrados.                                   |
| HU14 | Como adotante, quero conversar com a ONG pelo chat, para tirar dúvidas sobre o animal e o processo de adoção.                                                      |
| HU15 | Como ONG, quero responder mensagens pelo chat, para orientar os adotantes interessados.                                                                            |
| HU16 | Como adotante, quero visualizar a distância aproximada entre minha localização e o local do animal anunciado, para saber quais animais estão mais próximos de mim. |
| HU17 | Como adotante, quero visualizar a localização aproximada do animal em um mapa, para entender melhor onde ele se encontra antes de solicitar a adoção.              |

---

## 🏗 Arquitetura

O **PetCar** utiliza uma arquitetura monolítica em camadas, adequada para um sistema acadêmico com funcionalidades concentradas em um mesmo domínio. A organização em camadas facilita a manutenção, a separação de responsabilidades e a compreensão do funcionamento geral da aplicação.

A arquitetura é composta por:

* **Frontend Web:** interface utilizada por adotantes e ONGs;
* **Camada REST API:** responsável por expor os endpoints do sistema;
* **Backend PetCar:** responsável pelas regras de negócio;
* **Banco de Dados PostgreSQL:** responsável pela persistência das informações;
* **API Externa de Mapas/Localização:** responsável pelo cálculo de distância e exibição da localização aproximada.

### Principais módulos do Backend

* **Módulo de Animais:** cadastro, edição, listagem e filtros;
* **Módulo de Adoção:** solicitação, análise e alteração de status;
* **Módulo de Chat:** envio e histórico de mensagens;
* **Módulo de Notificações:** geração de alertas para usuários;
* **Módulo de Localização:** cálculo de distância e integração com API externa.

---

## 📊 Diagramas do Projeto

Os diagramas do sistema estão organizados na pasta **`Diagrama Imagens`**.

### Diagramas principais

| Diagrama                 | Imagem                                                                     |
| ------------------------ | -------------------------------------------------------------------------- |
| Diagrama de Casos de Uso | <img src="Diagrama%20Imagens/Diagrama%20Casos%20de%20Uso.png" width="350"> |
| Diagrama de Classes      | <img src="Diagrama%20Imagens/Diagrama%20Classes.png" width="350">          |
| Diagrama de Arquitetura  | <img src="Diagrama%20Imagens/Diagrama%20de%20Arquitetura.png" width="350"> |
| Diagrama de Componentes  | <img src="Diagrama%20Imagens/Diagrama%20de%20Componentes.png" width="350"> |
| Diagrama de Implantação  | <img src="Diagrama%20Imagens/Diagrama%20de%20Implantação.png" width="350"> |
| Modelo de Banco          | <img src="Diagrama%20Imagens/Modelos%20de%20Banco.png" width="350">        |

---

### Diagramas de Sequência

| Diagrama                    | Imagem                                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Solicitação de adoção       | <img src="Diagrama%20Imagens/Diagrama%20de%20Sequencia%20-%20Solicitação%20de%20adoção.png" width="350">     |
| Analisar solicitação        | <img src="Diagrama%20Imagens/Diagrama%20de%20Sequencia%20-%20Analisar%20Solicitação.png" width="350">        |
| Enviar mensagem             | <img src="Diagrama%20Imagens/Diagrama%20de%20Sequencia%20-%20Enviar%20mensagem.png" width="350">             |
| Cadastrar animal            | <img src="Diagrama%20Imagens/Diagrama%20de%20Sequencia%20-%20Cadastrar%20Animal.png" width="350">            |
| Consultar e filtrar animais | <img src="Diagrama%20Imagens/Diagrama%20de%20Sequencia%20-%20Consultar%20e%20Filtrar.png" width="350">       |
| Localização e proximidade   | <img src="Diagrama%20Imagens/Diagrama%20de%20Sequencia%20-%20Localização%20e%20proximidade.png" width="350"> |

---

### Diagramas de Comunicação

| Diagrama              | Imagem                                                                                                  |
| --------------------- | ------------------------------------------------------------------------------------------------------- |
| Solicitação de adoção | <img src="Diagrama%20Imagens/Diagrama%20de%20Comunicação%20-%20Solicitação%20Adoção.png" width="350">   |
| Analisar solicitação  | <img src="Diagrama%20Imagens/Diagrama%20de%20Comunicação%20-%20Analisar%20Solicitação.png" width="350"> |
| Enviar mensagem       | <img src="Diagrama%20Imagens/Diagrama%20de%20Comunicação%20-%20Enviar%20mensagem.png" width="350">      |
| Consultar animais     | <img src="Diagrama%20Imagens/Diagrama%20de%20Comunicação%20-%20Consultar%20Animais.png" width="350">    |

---

### Diagramas de Estado

| Diagrama                        | Imagem                                                                                                |
| ------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Estado do Animal                | <img src="Diagrama%20Imagens/Diagrama%20de%20Estado%20-%20Animal.png" width="350">                    |
| Estado do Chat                  | <img src="Diagrama%20Imagens/Diagrama%20de%20Estado%20-%20Chat.png" width="350">                      |
| Estado da Solicitação de Adoção | <img src="Diagrama%20Imagens/Diagrama%20de%20Estado%20-%20Solicitação%20de%20Adoção.png" width="350"> |

---

## 🗃 Modelo de Dados

O sistema utiliza banco de dados relacional **PostgreSQL**. As principais tabelas previstas são:

* `usuario`;
* `adotante`;
* `ong`;
* `animal`;
* `solicitacao_adocao`;
* `chat`;
* `mensagem`;
* `notificacao`.

### Relacionamentos principais

* Um usuário pode ser um adotante ou uma ONG;
* Uma ONG pode cadastrar vários animais;
* Um adotante pode realizar várias solicitações de adoção;
* Um animal pode receber várias solicitações;
* Uma solicitação pode possuir um chat;
* Um chat pode conter várias mensagens;
* Um usuário pode receber várias notificações;
* Uma solicitação pode gerar várias notificações.

A API de localização não possui tabela própria, pois representa um serviço externo. Os dados necessários para seu uso, como cidade, estado, latitude e longitude, são armazenados nas entidades `adotante`, `ong` e `animal`.

---

## 📂 Estrutura de Pastas

```text
PETCARE
├── Diagrama Imagens
│   ├── Diagrama Casos de Uso.png
│   ├── Diagrama Classes.png
│   ├── Diagrama de Arquitetura.png
│   ├── Diagrama de Componentes.png
│   ├── Diagrama de Comunicação - Analisar Solicitação.png
│   ├── Diagrama de Comunicação - Consultar Animais.png
│   ├── Diagrama de Comunicação - Enviar mensagem.png
│   ├── Diagrama de Comunicação - Solicitação Adoção.png
│   ├── Diagrama de Estado - Animal.png
│   ├── Diagrama de Estado - Chat.png
│   ├── Diagrama de Estado - Solicitação de Adoção.png
│   ├── Diagrama de Implantação.png
│   ├── Diagrama de Sequencia - Cadastrar Animal.png
│   ├── Diagrama de Sequencia - Consultar e Filtrar.png
│   ├── Diagrama de Sequencia - Localização e proximidade.png
│   ├── Diagrama de Sequencia - Analisar Solicitação.png
│   ├── Diagrama de Sequencia - Enviar mensagem.png
│   ├── Diagrama de Sequencia - Solicitação de adoção.png
│   └── Modelos de Banco.png
│
├── Diagramas puml
│   └── Arquivos .puml dos diagramas
│
└── README.md
```

---

## 🧪 Testes

Por se tratar de um projeto de documentação e modelagem, os testes foram planejados com base nos principais fluxos do sistema.

### Casos de teste previstos

* Cadastro de animal pela ONG;
* Edição dos dados do animal;
* Listagem de animais disponíveis;
* Aplicação de filtros por espécie, porte, idade e localização;
* Visualização da ficha do animal;
* Cálculo de distância aproximada;
* Solicitação de adoção pelo adotante;
* Análise da solicitação pela ONG;
* Alteração do status da adoção;
* Envio de notificação ao adotante;
* Envio de mensagem pelo chat;
* Consulta do histórico de solicitações.

---

## 📌 Status dos Animais

Os animais cadastrados podem possuir os seguintes estados:

* **Disponível:** animal visível para adoção;
* **Em processo de adoção:** existe solicitação em análise;
* **Adotado:** solicitação aprovada;
* **Indisponível:** animal removido ou temporariamente ocultado.

---

## 📌 Status das Solicitações

As solicitações de adoção podem possuir os seguintes estados:

* **Enviada:** solicitação criada pelo adotante;
* **Em análise:** solicitação visualizada ou avaliada pela ONG;
* **Aprovada:** pedido aceito pela ONG;
* **Recusada:** pedido negado pela ONG;
* **Cancelada:** pedido cancelado antes da finalização.

---

## 📌 Histórico de Revisões

| Nome           | Data     | Razões para Mudança                                                                                                              | Versão |
| -------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------- | ------ |
| Diogo Henrique | 07/06/26 | Criação do repositório                                                                                                           | 0.1    |
| Diogo Henrique | 07/06/26 | Inclusão do diagrama de casos de uso e dos diagramas de sequência iniciais                                                       | 0.2    |
| Diogo Henrique | 08/06/26 | Inclusão dos diagramas de arquitetura, implantação e classes; atualização dos casos de uso e histórias de usuário                | 0.3    |
| Diogo Henrique | 09/06/26 | Inclusão dos diagramas de sequência, comunicação e estados; inclusão do modelo de dados e atualização do diagrama de componentes | 0.4    |
| Diogo Henrique | 10/06/26 | Atualização do README e revisão final da documentação                                                                            | 1.0    |

---

## 📖 Documentações utilizadas

* Documentação oficial do PlantUML;
* Documentação oficial do PostgreSQL;
* Materiais da disciplina Projeto de Software;
* Template de documentação fornecido para o trabalho;
* Diagramas UML desenvolvidos para o sistema PetCar.

---

## 👥 Autores

| Nome                            | Curso                  | Instituição |
| ------------------------------- | ---------------------- | ----------- |
| Diogo Henrique Moreira da Silva | Engenharia de Software | PUC Minas   |

---

## 🙏 Agradecimentos

Agradecimentos à **PUC Minas** e à disciplina **Projeto de Software**, pelo desenvolvimento dos conhecimentos relacionados à modelagem, documentação e arquitetura de sistemas.

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos.

---
