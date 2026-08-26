# Arquitetura e Modelagem — LNCrochetAI

## 1. Introdução

Este documento apresenta a modelagem inicial da plataforma CrochetAI, contemplando o fluxo principal do sistema, a arquitetura proposta, o modelo inicial de dados e os protótipos das principais interfaces da aplicação.

## 2. Fluxograma geral do sistema

O fluxo geral representa as principais etapas realizadas pelo usuário desde o acesso à plataforma até a obtenção de uma receita ou resultado de busca.

```mermaid
flowchart TD
    A[Usuário acessa o CrochetAI] --> B{Escolhe uma opção}

    B --> C[Enviar imagem]
    B --> D[Criar ou personalizar receita]

    C --> E[Sistema recebe a imagem]
    E --> F[Análise da imagem]
    F --> G[Busca por receitas semelhantes]
    G --> H{Resultados encontrados?}

    H -->|Sim| I[Apresentar resultados]
    H -->|Não| J[Auxiliar na criação da receita]

    D --> K[Usuário informa medidas e preferências]
    K --> L[Processamento pela Inteligência Artificial]
    L --> M[Gerar receita personalizada]

    I --> N[Usuário analisa o resultado]
    J --> N
    M --> N
```

## 3. Arquitetura do sistema

A arquitetura proposta apresenta os principais componentes da plataforma e a comunicação entre eles. O usuário interage com a interface da aplicação, que se comunica com o backend responsável pelo processamento das informações e integração com os demais serviços.

```mermaid
flowchart TD
    U[Usuário] --> F[Frontend]

    F --> B[Backend]

    B --> BD[(Banco de Dados)]
    B --> IA[Serviço de Inteligência Artificial]
    B --> VC[Visão Computacional]
    B --> BS[Mecanismo de Busca]

    IA --> B
    VC --> B
    BS --> B

    B --> F
    F --> U
```

## 4. Modelo de dados

O modelo de dados representa as principais informações que deverão ser armazenadas pelo sistema e seus relacionamentos.

```mermaid
erDiagram
    USUARIO ||--o{ PESQUISA : realiza
    USUARIO ||--o{ RECEITA_PERSONALIZADA : cria
    RECEITA ||--o{ RECEITA_PERSONALIZADA : possui

    USUARIO {
        int id
        string nome
        string email
        string senha
    }

    PESQUISA {
        int id
        int usuario_id
        string imagem
        date data
    }

    RECEITA {
        int id
        string nome
        string categoria
        string dificuldade
        string fonte
    }

    RECEITA_PERSONALIZADA {
        int id
        int usuario_id
        int receita_id
        string medidas
        string fio
        string agulha
    }
```

## 5. Fluxo da busca por imagem

A busca por imagem representa uma das principais funcionalidades do CrochetAI. O usuário envia uma fotografia de uma peça, que será analisada pelo sistema para auxiliar na localização de peças ou receitas semelhantes.

```mermaid
flowchart TD
    A[Usuário seleciona uma imagem] --> B[Upload da imagem]
    B --> C[Processamento da imagem]
    C --> D[Análise por visão computacional]
    D --> E[Busca por peças semelhantes]
    E --> F{Encontrou resultados?}

    F -->|Sim| G[Exibir resultados]
    F -->|Não| H[Auxiliar na criação de uma receita]

    G --> I[Usuário acessa a fonte da receita]
    H --> J[Usuário fornece informações adicionais]
    J --> K[IA auxilia na criação da receita]
```

## 6. Fluxo de criação e personalização de receitas

O usuário poderá fornecer informações sobre a peça desejada, suas medidas e preferências. Essas informações serão utilizadas para auxiliar na elaboração ou adaptação de uma receita.

```mermaid
flowchart TD
    A[Usuário informa características da peça] --> B[Informa medidas]
    B --> C[Informa material e agulha]
    C --> D[Informa pontos e preferências]
    D --> E[Processamento das informações]
    E --> F[Inteligência Artificial]
    F --> G[Cálculos de pontos e carreiras]
    G --> H[Receita personalizada]
    H --> I[Usuário analisa e ajusta]
```

## 7. Protótipos de interface

Os protótipos iniciais da plataforma serão desenvolvidos para representar as principais telas e interações previstas para o sistema.

As telas previstas são:

- Página inicial;
- Busca por imagem;
- Resultados da busca;
- Criação de receita;
- Personalização de receita.

### Página inicial

A página inicial deverá apresentar as principais funcionalidades da plataforma e permitir que o usuário escolha entre buscar uma receita por imagem ou criar e personalizar uma receita.

### Busca por imagem

A tela deverá permitir que o usuário envie uma imagem da peça de crochê que deseja pesquisar.

### Resultados

A tela deverá apresentar os resultados encontrados pelo sistema, incluindo peças ou receitas semelhantes e suas respectivas fontes.

### Criação de receita

A tela deverá permitir que o usuário informe características da peça, como tamanho, medidas, fio, agulha e ponto.

### Personalização

A tela deverá permitir que o usuário adapte uma receita de acordo com suas medidas e preferências.

## 8. Tecnologias previstas

As tecnologias inicialmente previstas para o desenvolvimento da plataforma são:

- HTML5;
- CSS3;
- JavaScript;
- Node.js;
- Banco de dados;
- APIs de Inteligência Artificial;
- Tecnologias de visão computacional;
- Git e GitHub.

As tecnologias poderão ser ajustadas durante o desenvolvimento do projeto.
