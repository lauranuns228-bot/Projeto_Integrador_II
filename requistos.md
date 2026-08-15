# 📋 Documento de Requisitos — LncrochetAI

## 1. Identificação do projeto

**Nome:** LncrochetAI — Plataforma Inteligente para Crochê

**Tipo:** Plataforma web

**Finalidade:** Projeto Integrador

**Status:** Levantamento inicial de requisitos
# 2. Introdução

O lncrochetAI consiste no desenvolvimento de uma plataforma web destinada a auxiliar pessoas que praticam crochê na localização, criação e adaptação de receitas.

O sistema utilizará recursos de Inteligência Artificial, visão computacional e processamento de informações para analisar imagens, pesquisar peças semelhantes e auxiliar na elaboração de receitas personalizadas.
 3. Problema

Usuários de crochê podem encontrar dificuldades para localizar uma receita específica quando possuem apenas uma imagem da peça desejada.

Além disso, uma receita encontrada pode não estar adequada às medidas, materiais ou preferências do usuário, tornando necessária uma adaptação manual.

O sistema proposto busca centralizar essas funcionalidades em uma única plataforma.
 4. Objetivo do sistema

Desenvolver uma plataforma capaz de:

* Receber imagens de peças de crochê;
* Identificar características dessas peças;
* Localizar receitas ou peças semelhantes;
* Apresentar as fontes originais dos resultados;
* Auxiliar na criação de receitas;
* Auxiliar na adaptação de receitas;
* Realizar cálculos relacionados às medidas da peça.

## 5.1 Usuário comum

Pessoa que utiliza a plataforma para:

* Pesquisar receitas;
* Enviar imagens;
* Consultar resultados;
* Criar receitas personalizadas;
* Adaptar receitas;
* Informar suas medidas e preferências.

## 5.2 Administrador

Responsável pelo gerenciamento da plataforma, incluindo:

* Gerenciamento de usuários;
* Gerenciamento de conteúdos cadastrados;
* Monitoramento do sistema;
* Administração do banco de dados;
* Controle de informações utilizadas pela plataforma.

# 6. Escopo

## 6.1 Funcionalidades incluídas

O sistema deverá contemplar inicialmente:

1. Cadastro e gerenciamento de usuários;
2. Envio de imagens;
3. Análise de imagens;
4. Busca por peças semelhantes;
5. Apresentação de resultados;
6. Direcionamento para fontes externas;
7. Criação de receitas com auxílio de IA;
8. Adaptação de receitas;
9. Inserção de medidas;
10. Cálculos de pontos e carreiras;
11. Armazenamento de informações relevantes.

## 6.2 Funcionalidades fora do escopo inicial

Não fazem parte da primeira versão:

* Venda de materiais de crochê;
* Venda de receitas;
* Reprodução integral e não autorizada de receitas de terceiros;
* Produção física das peças;
* Garantia de que uma receita gerada automaticamente estará livre de erros.
# 7. Requisitos funcionais

### RF01 — Cadastro de usuário

O sistema deverá permitir que o usuário realize seu cadastro na plataforma.

### RF02 — Login

O sistema deverá permitir que usuários cadastrados realizem autenticação.

### RF03 — Envio de imagem

O sistema deverá permitir que o usuário envie uma imagem de uma peça de crochê.

### RF04 — Análise da imagem

O sistema deverá processar a imagem enviada e identificar características relevantes da peça.

### RF05 — Classificação da peça

O sistema deverá tentar classificar a peça de acordo com categorias previamente definidas, como:

* Amigurumi;
* Roupa;
* Bolsa;
* Acessório;
* Decoração;
* Tapete;
* Outros.

### RF06 — Busca de peças semelhantes

O sistema deverá utilizar as características identificadas para localizar peças ou receitas semelhantes.

### RF07 — Apresentação dos resultados

O sistema deverá apresentar os resultados encontrados de maneira organizada.

### RF08 — Fonte original

Quando um resultado estiver associado a uma fonte externa, o sistema deverá apresentar o link para a fonte original.

### RF09 — Criação de receita

O sistema deverá permitir que o usuário forneça características de uma peça para solicitar auxílio na elaboração de uma receita.

### RF10 — Personalização

O sistema deverá permitir que o usuário informe características como:

* Medidas;
* Tamanho;
* Fio;
* Agulha;
* Pontos;
* Preferências de estilo.

### RF11 — Adaptação

O sistema deverá auxiliar na adaptação de uma receita de acordo com novas medidas ou parâmetros fornecidos.

### RF12 — Cálculo de pontos

O sistema deverá realizar cálculos relacionados à quantidade de pontos necessários para determinadas medidas, considerando os dados disponíveis.

### RF13 — Cálculo de carreiras

O sistema deverá auxiliar no cálculo da quantidade de carreiras necessárias para atingir determinada medida.

### RF14 — Histórico

O sistema poderá armazenar pesquisas e receitas geradas para consulta posterior pelo usuário.

### RF15 — Avaliação dos resultados

O sistema poderá permitir que o usuário avalie a utilidade ou qualidade de um resultado fornecido.

---

# 8. Requisitos não funcionais

Os requisitos não funcionais definem características relacionadas à **qualidade e funcionamento do sistema**.

### RNF01 — Usabilidade

A interface deverá ser simples e intuitiva, permitindo que usuários com diferentes níveis de conhecimento tecnológico utilizem a plataforma.

### RNF02 — Responsividade

A plataforma deverá apresentar uma interface adaptável a computadores, tablets e smartphones.

### RNF03 — Desempenho

O sistema deverá apresentar os resultados das operações em tempo adequado, considerando as limitações das APIs e serviços externos utilizados.

### RNF04 — Segurança

Os dados dos usuários deverão ser armazenados de forma segura e as informações sensíveis não deverão ser expostas indevidamente.

### RNF05 — Disponibilidade

A plataforma deverá permanecer disponível durante seu período de operação, considerando a infraestrutura utilizada.

### RNF06 — Manutenibilidade

O código deverá ser organizado de maneira que facilite futuras alterações, correções e inclusão de novas funcionalidades.

### RNF07 — Compatibilidade

O sistema deverá funcionar nos principais navegadores modernos.

### RNF08 — Privacidade

As imagens enviadas pelos usuários deverão ser tratadas de acordo com as políticas de privacidade definidas para o projeto.

---

# 9. Regras de negócio

### RN01

Uma imagem deverá ser enviada pelo usuário antes que o sistema possa realizar uma busca baseada em imagem.

### RN02

Os resultados de busca deverão apresentar, sempre que possível, a fonte original do conteúdo.

### RN03

O sistema não deverá disponibilizar automaticamente conteúdo protegido de terceiros sem autorização.

### RN04

Receitas geradas por Inteligência Artificial deverão ser apresentadas como sugestões e poderão exigir revisão do usuário.

### RN05

Os cálculos realizados pelo sistema deverão utilizar as medidas e parâmetros fornecidos pelo usuário.

### RN06

A precisão dos resultados de identificação dependerá da qualidade da imagem enviada e das informações disponíveis.

---

# 10. Entradas do sistema

O sistema poderá receber:

* Imagens;
* Medidas;
* Tipo de peça;
* Tamanho desejado;
* Tipo de fio;
* Espessura do fio;
* Tamanho da agulha;
* Tipo de ponto;
* Receita existente;
* Preferências do usuário.

---

# 11. Saídas do sistema

O sistema poderá fornecer:

* Peças semelhantes;
* Links para receitas;
* Classificação da peça;
* Características identificadas;
* Sugestões de pontos;
* Receitas personalizadas;
* Adaptações de receitas;
* Quantidade estimada de pontos;
* Quantidade estimada de carreiras;
* Orientações para o usuário.

---

# 12. Fluxo principal

```text
Usuário
   ↓
Acessa a plataforma
   ↓
Envia uma imagem ou informa as características da peça
   ↓
Sistema processa as informações
   ↓
IA analisa os dados
   ↓
Busca por peças/receitas semelhantes
   ↓
Resultados encontrados?
   ├── Sim → Apresentar resultados e fontes
   │
   └── Não → Oferecer criação de receita
                    ↓
              Usuário fornece medidas
                    ↓
              IA auxilia na elaboração
                    ↓
              Receita personalizada
```

---

# 13. Critérios de aceitação

O sistema será considerado funcional quando for capaz de:

* [ ] Receber uma imagem de uma peça;
* [ ] Processar a imagem;
* [ ] Retornar resultados relacionados à peça pesquisada;
* [ ] Apresentar fontes externas quando disponíveis;
* [ ] Receber medidas fornecidas pelo usuário;
* [ ] Utilizar essas medidas no processo de personalização;
* [ ] Gerar uma proposta de receita com auxílio de IA;
* [ ] Realizar cálculos básicos de pontos e carreiras;
* [ ] Apresentar os resultados de forma compreensível;
* [ ] Funcionar adequadamente em diferentes tamanhos de tela.

---

# 14. Limitações previstas

A identificação automática poderá apresentar resultados incorretos em situações como:

* Imagens com baixa qualidade;
* Peças parcialmente visíveis;
* Fotografias com pouca iluminação;
* Peças muito diferentes dos exemplos disponíveis;
* Ausência de informações suficientes para realizar os cálculos.

As receitas geradas por Inteligência Artificial também poderão necessitar de revisão e testes antes de serem utilizadas na produção de uma peça.

---

# 15. Considerações finais

O documento apresenta os requisitos iniciais do CrochetAI. Durante o desenvolvimento do projeto, os requisitos poderão ser revisados, detalhados ou modificados de acordo com os resultados dos testes, limitações técnicas e necessidades identificadas.

A documentação deverá ser atualizada sempre que ocorrer uma alteração significativa no escopo ou nas funcionalidades do sistema.

