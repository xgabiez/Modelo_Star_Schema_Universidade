# 🧩 Desafio DIO de Modelagem Dimensional – Star Schema

## 🎯 Objetivo
O objetivo deste desafio foi **analisar um modelo relacional existente** e transformá-lo em um **modelo dimensional (Star Schema)**, adequado para utilização em ferramentas de Business Intelligence, como o Power BI.

---

## 🧠 Etapas do Projeto

### 1. Análise do Modelo Relacional
Foi disponibilizado um **modelo relacional** contendo diversas tabelas relacionadas a professores, cursos, departamentos, disciplinas e outras entidades do contexto educacional.  
Durante a análise, foi possível identificar **as principais entidades e relacionamentos** relevantes para a construção do modelo dimensional.

### 2. Identificação das Tabelas Necessárias
A partir do modelo original, foram selecionadas apenas as tabelas **essenciais para a análise do problema**, com o foco em medir as **horas ministradas por professor**.  
As tabelas dimensionais definidas foram:

- `d_professor` – informações descritivas dos professores (nome, titulação, etc.);
- `d_curso` – dados sobre os cursos;
- `d_disciplina` – disciplinas ministradas;
- `d_departamento` – departamentos e campus;
- `d_data` – criada para representar o tempo (data e ano).

### 3. Criação da Tabela Fato
Foi criada a tabela **`fato_professor`**, centralizando as medidas do modelo.  
Essa tabela contém:
- Chaves estrangeiras das dimensões (FKs);
- A métrica **`horas_ministradas`**, do tipo `DECIMAL`, representando a quantidade de horas lecionadas por professor.

Essa estrutura segue o padrão **1:N** entre dimensões e fato, garantindo integridade e boa performance analítica.

---

## 🖼️ Modelo Dimensional (Star Schema)

Abaixo está a representação visual do modelo criado:

![Modelo Star Schema](Universidade_Start_Schema_nova.png)

---

## 🧾 Ferramentas Utilizadas
- **MySQL Workbench** – modelagem e criação do diagrama entidade-relacionamento;
- **GitHub** – versionamento e publicação do desafio;
- **Power BI** (posteriormente aplicável) – ferramenta de análise para consumo do modelo dimensional.

---

## 📊 Resultado
O modelo final segue o padrão **Star Schema**, com:
- Uma **tabela fato** central;
- Cinco **tabelas dimensão** conectadas por chaves estrangeiras;
- Estrutura pronta para ser utilizada em análises de BI (como horas ministradas por professor, curso, disciplina, departamento e período).



