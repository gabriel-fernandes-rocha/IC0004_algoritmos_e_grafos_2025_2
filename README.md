# Caminho Hamiltoniano: Complexidade, Algoritmos e Experimentos

## Sobre o Projeto
Trabalho prático da disciplina IC0004 - Algoritmos e Grafos (2025.2) do curso de Pós-Graduação em Ciência da Computação da Universidade Federal da Bahia (UFBA).
Este projeto explora o Problema do Caminho Hamiltoniano em grafos gerais. O estudo aborda desde a fundamentação teórica (prova de NP-Completude via redução polinomial) até a implementação prática e análise experimental de algoritmos exatos e heurísticos.

## Como Executar
#### Opção 1: Google Colab (Recomendado)

Acesse o notebook no Google Colab:

   https://colab.research.google.com/

Faça upload do arquivo Reducao_Polinomial__Parte_C__Parte_D.ipynb
Faça upload do arquivo grafo_teste.txt para o seu Google Drive
Altere o caminho do arquivo no código:

python   caminho_do_arquivo = "/content/drive/MyDrive/seu_caminho/grafo_teste.txt"

Execute todas as células sequencialmente

#### Opção 2: Ambiente Local
Pré-requisitos
bashPython 3.10+
pip install networkx matplotlib pandas numpy openpyxl psutil
Execução
bash# Clone o repositório
git clone https://github.com/gabriel-fernandes-rocha/IC0004_algoritmos_e_grafos_2025_2.git
cd IC0004_algoritmos_e_grafos_2025_2

Execute o notebook (ou converta para .py)
jupyter notebook Reducao_Polinomial__Parte_C__Parte_D.ipynb

## Formato do Arquivo de Entrada
O programa lê grafos não-direcionados no seguinte formato:

n m

u1 v1

u2 v2

...

um vm

Onde:

n = número de vértices (indexados de 0 a n-1)
m = número de arestas
Cada linha seguinte representa uma aresta (ui, vi)

Exemplo (grafo_teste.txt):

10 11

0 1

0 4

1 2

1 3

2 5

2 6

3 7

4 5

6 7

7 8

8 9

Este grafo possui 10 vértices e 11 arestas, formando uma estrutura conexa que contém um Caminho Hamiltoniano.

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
