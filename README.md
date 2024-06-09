## Desafio de Projeto Dashboard de Vendas com Power BI utilizando Star Schema

**DIO - Bootcamp Data Analytics com Power BI**

# Desafio Star Schema para Análise de Dados de Professores

## Descrição do Desafio

O objetivo deste desafio é criar um esquema dimensional (Star Schema) para análise de dados focado nos professores. O esquema deve refletir as informações dos professores, cursos ministrados, departamentos e outras métricas relevantes para permitir uma análise detalhada do desempenho e das atividades dos professores.

### Componentes do Star Schema

1. **Tabela Fato (Fato_Professor)**:
   - **Professor_ID**: Chave estrangeira referenciando a dimensão do Professor.
   - **Curso_ID**: Chave estrangeira referenciando a dimensão do Curso.
   - **Departamento_ID**: Chave estrangeira referenciando a dimensão do Departamento.
   - **Data_ID**: Chave estrangeira referenciando a dimensão de Data.
   - **Número_de_Aulas**: Quantidade de aulas ministradas.
   - **Horas_Ensino**: Total de horas de ensino.
   - **Avaliação_Média**: Avaliação média recebida.
   - **Salário**: Salário do professor.

2. **Tabelas de Dimensão**:
   - **Dim_Professor**:
     - **Professor_ID**: Chave primária.
     - **Nome**: Nome completo do professor.
     - **Gênero**: Gênero do professor.
     - **Data_Nascimento**: Data de nascimento do professor.
     - **Grau_Acadêmico**: Grau acadêmico mais alto do professor.
     - **Data_Contratação**: Data de contratação do professor.
   
   - **Dim_Curso**:
     - **Curso_ID**: Chave primária.
     - **Nome_Curso**: Nome do curso.
     - **Departamento_ID**: Chave estrangeira referenciando a dimensão do Departamento.
     - **Nível**: Nível do curso (graduação, pós-graduação, etc.).
     - **Créditos**: Número de créditos do curso.
     - **Duração_Semanas**: Duração do curso em semanas.
   
   - **Dim_Departamento**:
     - **Departamento_ID**: Chave primária.
     - **Nome_Departamento**: Nome do departamento.
     - **Faculdade**: Faculdade à qual o departamento pertence.
     - **Chefe_Departamento**: Nome do chefe do departamento.

   - **Dim_Data**:
     - **Data_ID**: Chave primária.
     - **Data**: Data no formato YYYY-MM-DD.
     - **Ano**: Ano da data.
     - **Mês**: Mês da data.
     - **Dia**: Dia do mês da data.
     - **Trimestre**: Trimestre da data.
     - **Semana_do_Ano**: Número da semana no ano.

### Instruções para Implementação

1. **Modelagem**: Utilize as informações fornecidas no diagrama relacional disponibilizado para criar o esquema em estrela.
2. **Datas**: Crie a tabela de dimensão de Data, supondo dados de datas de oferta de disciplinas e cursos.
3. **Granularidade**: Considere a granularidade apropriada para a análise dos dados dos professores.
4. **Documentação**: Documente seu esquema estrela, incluindo as tabelas de fato e dimensão, além de explicações sobre a granularidade e decisões de modelagem.

### Exemplo de Uso

Para analisar o desempenho de um professor específico ao longo do tempo, você pode utilizar o esquema estrela para consultar métricas como número de aulas ministradas, horas de ensino, e avaliações médias, filtrando por professor e período de tempo.
