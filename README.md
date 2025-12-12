# Detecção de Fraude em Sinistros de Seguros – Pipeline de Inferência Multi-Modelo

Este projeto demonstra uma arquitetura de modelo múltiplo (Multi-Model AI) para identificar sinistros de seguros fraudulentos. O pipeline de inferência utiliza técnicas 
avançadas de Inteligência Artificial (IA) e Machine Learning (ML), aproveitando o poder de processamento do IBM z17.

## Contexto
A fraude em sinistros de seguros representa um desafio significativo para as seguradoras. A implementação de modelos de IA/ML visa sinalizar rapidamente sinistros suspeitos, 
resultando na redução de perdas financeiras e na melhoria da eficiência operacional.

## Desafio
Uma grande seguradora busca aprimorar seu processo de ajuste de sinistros, que atualmente envolve tanto dados estruturados quanto dados não estruturados (como textos de 
descrições dos sinistros).

O objetivo é:

    Alavancar a IA para autojulgar sinistros de baixo risco.

    Reduzir o tempo de ajuste do sinistro.

    Minimizar o trabalho de investigação manual.


## Solução e Arquitetura Multi-Modelo
A solução implementa uma arquitetura de IA com múltiplos modelos, projetada para lidar com a complexidade dos dados estruturados e não estruturados de um sinistro:

    Processamento de Dados Não Estruturados (BERT):

        Dados de sinistros não estruturados são processados por um Encoder LLM (BERT).

        O BERT extrai, categoriza e classifica informações-chave do texto.

        As features (características) extraídas são anexadas às tabelas de dados estruturados.

    Detecção Preditiva de Fraude (XGBoost):

        Um modelo preditivo de detecção de fraude (XGBoost) pontua o sinistro, combinando os dados estruturados originais com as features extraídas pelo BERT.

        O modelo identifica padrões de alto risco e sinaliza reclamações com potencial de fraude.



## Tecnologias e Modelos
Plataforma de Execução: IBM z17
Modelos de IA/ML Utilizados:

        BERT LLM: Utilizado para Feature Extraction (Extração de Características) de dados não estruturados.

        XGBoost (eXtreme Gradient Boosting): Modelo preditivo para a classificação de risco de fraude.

## Produtos Alavançados:

        AI Toolkit for IBM Z & LinuxONE

        Machine learning for IBM z/OS


## Conclusão: 
O pipeline de inferência demonstrou a integração bem-sucedida de dados estruturados e não estruturados no IBM z17 para a detecção de fraudes.

O uso do BERT para extração de features e do XGBoost para pontuação de risco permitiu uma identificação precisa e automatizada de sinistros, resultando em:

    Identificação automática de sinistros de baixo risco e potencialmente fraudulentos.

    Redução do esforço manual no processo de ajuste.

    Melhoria da eficiência geral no processamento de sinistros.
