# 📊 Pipeline de Telemetria - Processamento de Dados Médicos

Um pipeline em Python para ETL (Extract, Transform, Load) e análise preditiva de dados de telemetria. Sendo assim, será feito a limpeza, validação e análise de dados de telemetria médica, com foco em qualidade de dados e detecção de anomalias.

## 🚀 Sobre o Projeto

Este projeto implementa um sistema de processamento de dados de pacientes que:
- **Valida** a integridade dos dados de entrada
- **Limpa** registros inconsistentes ou incompletos
- **Detecta** valores médicos fora dos parâmetros esperados
- **Gera** relatórios para análise posterior

## 📋 Esquema de Dados

|     Campo     |  Tipo  |              Descrição                |
|---------------|--------|---------------------------------------|
| `ID`          | string | Identificador único do paciente       |
| `pressao`     | int    | Valor da pressão arterial             |
| `saturacao`   | int    | Nível de saturação de oxigênio (%)    |
| `temperatura` | float  | Temperatura corporal em graus Celsius |


## 📋 Funcionalidades Principais

### ✅ Validação de Dados
- Remove linhas com atributos em branco
- Filtra dados que não podem ser convertidos para seus determinados tipos
- Mantém integridade dos dados válidos

### 📊 Sistema de Arquivos de Saída

#### 📈 **Dados Processados**
- **`pacientes_monitorados.json`** - Todos os dados validados e limpos, usando `ID do paciente` como chave

#### 📝 **Logs e Relatórios**
- **`telemetria.txt`** - Log dos dados de entrada recebidos
- **`log_erros.txt`** - Registra todos os dados rejeitados durante a limpeza e o motivo de sua rejeição
- **`relatorio_de_alertas.txt`** - Salva valores médicos fora dos parâmetros normais

## 🛠 Tecnologias Utilizadas

- **Python 3.11**
- **JSON** - Armazenamento estruturado dos dados processados
