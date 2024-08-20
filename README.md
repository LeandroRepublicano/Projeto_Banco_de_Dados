# Projeto_Banco_de_Dados

Este projeto faz parte da trilha de Data Science do Santander Coders em parceria com a ADA Tech. O desafio consistiu em criar um banco de dados no PostgreSQL e, a partir dele, realizar uma análise utilizando bases de dados escolhidas ao longo das aulas. A proposta central foi explorar a criação e o gerenciamento de tabelas relacionais, além de conduzir análises descritivas baseadas nos dados armazenados.

## Estrutura do Banco de Dados

Para este projeto, selecionei duas bases de dados complementares, que se relacionam através de uma chave primária/estrangeira, permitindo análises integradas:

1. **Tabela `eventos`:**
    - `IDEvento` (INT): Identificador único do evento, utilizado como chave primária.
    - `CaminhoEvento` (VARCHAR): Local ou caminho onde o evento será realizado. 
    - `Federacao` (VARCHAR): Federação responsável pela organização do evento.
    - `Data` (DATE): Data em que o evento foi realizado.
    - `PaisEvento` (VARCHAR): País onde o evento ocorreu.
    - `EstadoEvento` (VARCHAR): Estado onde ocorreu o evento.
    - `CidadeEvento` (VARCHAR): Cidade onde ocorreu evento.
    - `NomeEvento` (VARCHAR): Nome completo do evento.

2. **Tabela `levantamento_peso`:**
    - `IDEvento` (INT): Chave estrangeira que se refere ao `IDEvento` na tabela `eventos`, permitindo associar cada levantamento a um evento específico. 
    - `Nome` (VARCHAR): Nome completo do atleta participante.
    - `Sexo` (VARCHAR): Sexo do atleta.
    - `Equipamento` (VARCHAR): Equipamento utilizado pelo atleta durante a competição, como "Raw" ou "Equipado".
    - `Idade` (INT): Idade do atleta, com uma restrição para garantir que não seja um valor negativo.
    - `Divisao` (VARCHAR): Divisão na qual o atleta competiu, categorizada por fatores como idade ou nível de habilidade.
    - `PesoCorporalKg` (NUMERIC): Peso corporal do atleta em quilogramas.
    - `ClassePesoKg` (VARCHAR): Classe de peso na qual o atleta compete, como "Até 74kg" ou "Acima de 120kg".
    - `MelhorAgachamentoKg` (NUMERIC): Melhor desempenho do atleta no agachamento em quilogramas.
    - `MelhorSupinoKg` (NUMERIC): Melhor desempenho do atleta no supino em quilogramas.
    - `MelhorLevantamentoTerraKg` (NUMERIC): Melhor desempenho do atleta no levantamento terra em quilogramas.
    - `TotalKg` (NUMERIC): Soma total dos melhores pesos levantados pelo atleta em todos os exercícios.
    - `Posicao` (VARCHAR): Posição final do atleta na competição, representada por números ordinais (1º, 2º, 3º, etc.).

## Análises Realizadas

Com as tabelas criadas e os dados inseridos, foi possível realizar uma série de análises descritivas que fornecem uma visão abrangente dos eventos e do desempenho dos atletas:

- **Distribuição de Eventos por Estado e Cidade:** Identificação das regiões com maior concentração de eventos, o que pode indicar áreas de maior interesse ou tradição no levantamento de peso.
- **Desempenho por Classe de Peso:** Comparação do peso levantado pelos atletas em diferentes classes de peso, fornecendo insights sobre a competitividade e os limites de desempenho em cada categoria.
- **Relação entre Peso dos Atletas e Peso Levantado:** Exploração da correlação entre o peso corporal dos atletas e o peso que conseguiram levantar, oferecendo uma análise sobre como o peso do atleta pode influenciar sua capacidade de desempenho nos diferentes exercícios.

## Perguntas Respondidas

Durante o desenvolvimento do projeto, elaborei e respondi a 10 perguntas específicas utilizando os dados disponíveis. Essas perguntas ajudaram a aprofundar a análise e a entender melhor os padrões observados. Entre as perguntas respondidas, destacam-se:

1. **Quais estados realizaram mais eventos?**
2. **Qual foi o maior peso levantado em cada classe?**
3. **Existe uma diferença significativa entre os pesos levantados por atletas de diferentes sexos?**
4. **Qual a relação entre o peso do atleta e o peso levantado?**

Essas e outras perguntas permitiram uma exploração detalhada dos dados, fornecendo insights valiosos que poderiam ser utilizados para melhorar a organização dos eventos e o treinamento dos atletas.

## Conclusões

Este projeto permitiu a exploração de diferentes aspectos do levantamento de peso, desde a organização de eventos até o desempenho dos atletas. Através do relacionamento entre as tabelas, foi possível obter insights valiosos e responder a perguntas que ajudam a entender melhor os dados. A análise demonstrou como o uso de um banco de dados relacional pode facilitar a gestão e a extração de informações em projetos de análise de dados complexos.

