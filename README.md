# Caminho Hamiltoniano: Complexidade, Algoritmos e Experimentos

## Sobre o Projeto
Trabalho prático da disciplina IC0004 - Algoritmos e Grafos (2025.2) do curso de Pós-Graduação em Ciência da Computação da Universidade Federal da Bahia (UFBA).
Este projeto explora o Problema do Caminho Hamiltoniano em grafos gerais. O estudo aborda desde a fundamentação teórica (prova de NP-Completude via redução polinomial) até a implementação prática e análise experimental de algoritmos exatos e heurísticos.

## Como Executar
#### Opção 1: Google Colab (Recomendado)

Acesse o notebook no Google Colab nesse Driver:

   https://drive.google.com/drive/folders/1IDx6XDRn6o4P0QA36qPKS0mQGPKy4keK?usp=drive_link

Altere o caminho do arquivo no código:

   caminho_do_arquivo = "/content/drive/MyDrive/seu_caminho/grafo_teste.txt"

Execute todas as células sequencialmente

#### Opção 2: Ambiente Local
Pré-requisitos
bash Python 3.10+
pip install networkx matplotlib pandas numpy openpyxl psutil
Execução
bash# Clone o repositório
git clone https://github.com/gabriel-fernandes-rocha/IC0004_algoritmos_e_grafos_2025_2.git
cd IC0004_algoritmos_e_grafos_2025_2

Execute o notebook (ou converta para .py)
jupyter notebook Reducao_Polinomial__Parte_C__Parte_D.ipynb

## Algoritmos Implementados
1. Algoritmo Exato - Backtracking Recursivo

Complexidade: O(n!) no pior caso
Garantia: 100% de corretude (sem falsos negativos)
Limitação: Intratável para n > 25 vértices
Estratégia: Busca em profundidade (DFS) com poda automática

pythonsolver.resolver_backtracking()  # Retorna "SIM" ou "NÃO"

2. Heurística Gulosa - Nearest Neighbor

Complexidade: O(n²)
Garantia: Nenhuma (pode gerar falsos negativos)
Vantagem: Escala para milhares de vértices
Estratégia: Escolha local gulosa sem backtracking

pythonsolver.resolver_heuristica()  # Retorna "SIM" ou "NÃO"
