
# ADR-001 - Arquitetura e Tecnologias do Connexa

**Situação:** aceita

**Data:** 2026-11-09

**Participantes:** Equipe de desenvolvimento Connexa

## Contexto

O projeto Connexa tem como objetivo facilitar a conexão
entre estudantes por meio da identificação de grupos
compatíveis com suas disciplinas, horários e disponibilidade.

O sistema precisa oferecer funcionalidades como cadastro
de estudantes, autenticação, verificação de vínculo
institucional, gerenciamento de disciplinas e horários,
descoberta de grupos compatíveis e solicitação de ingresso
em grupos.

Para atender essas necessidades, é necessário utilizar
uma arquitetura organizada, segura e de fácil manutenção,
permitindo que diferentes integrantes da equipe trabalhem
simultaneamente no desenvolvimento.

## Decisão

A equipe adotará uma arquitetura dividida em frontend
e backend.

As tecnologias utilizadas serão:

- **Frontend:** React, responsável pelas interfaces
  e pela interação com os usuários.
- **Backend:** Java com Spring Boot, responsável pelas
  regras de negócio e pelo processamento das solicitações.
- **Banco de dados:** PostgreSQL, responsável pelo
  armazenamento e gerenciamento das informações.

O frontend e o backend serão organizados separadamente,
permitindo a evolução independente de cada parte.

A comunicação entre frontend e backend será realizada
por meio de uma API REST, conforme a implementação
do projeto.

## Alternativas consideradas

| Alternativa | Motivo da não escolha |
|---|---|
| Angular | A equipe optou por utilizar React no frontend. |
| Vue.js | A equipe optou por utilizar React no frontend. |
| MySQL | A equipe adotou PostgreSQL como banco de dados. |
| Aplicação sem separação entre frontend e backend | A equipe optou pela separação das responsabilidades. |

## Consequências

**Positivas:**

- Melhor organização do código.
- Separação das responsabilidades.
- Facilidade de manutenção e evolução.
- Possibilidade de desenvolvimento paralelo.
- Utilização de tecnologias adequadas ao desenvolvimento web.
- Facilidade de integração entre frontend e backend.

**Negativas:**

- Necessidade de configurar a comunicação entre frontend e backend.
- Necessidade de gerenciar a conexão com o banco de dados.
- Maior cuidado com a integração entre os componentes.
- Necessidade de implementar mecanismos de segurança
  para proteger os dados dos estudantes.

**Como verificar:**

- Verificar se o frontend React inicia corretamente.
- Verificar se o backend Java com Spring Boot inicia corretamente.
- Verificar se a conexão com o PostgreSQL funciona.
- Testar a comunicação entre frontend e backend.
- Executar testes das funcionalidades implementadas.
- Verificar se os dados dos estudantes são armazenados
  e protegidos corretamente.

