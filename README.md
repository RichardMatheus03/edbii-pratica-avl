# Prática — Árvore AVL (EDB II)

Resolução da **Avaliação Prática Assíncrona: Árvore AVL** da disciplina **Estruturas de Dados Básicas II** (IMD0039, UFRN/IMD, 2026.2).

**Autor:** Richard Matheus Bezerra Ataliba

## Conteúdo

- `edbii-pratica-avl.ipynb`: notebook respondido e executado, com todas as saídas visíveis e todos os testes ✅.

## Questões

- **Ponto de partida:** reaproveita as classes `No` e `ArvoreBinariaBusca` da [Prática ABB](https://github.com/RichardMatheus03/edbii-pratica-bst).
- **Questão 1 — Implementando a AVL:** `AVLNode` herda de `No` e acrescenta `altura`. `AVLTree` herda de `ArvoreBinariaBusca` e implementa altura em O(1), fator de balanceamento, rotações simples (direita e esquerda), `balancear` (casos LL, LR, RR e RL), `adicionar` e `remover` recursivos com rebalanceamento na volta da recursão. Na remoção de um nó com dois filhos, usa o sucessor. Inclui um teste extra com inserções e remoções aleatórias que confere os invariantes da AVL (ordem de ABB, alturas corretas e |FB| ≤ 1).
- **Questão 2 — Pedidos numerados em sequência:** compara ABB e AVL com chaves inseridas em ordem crescente. Implementa o custo médio de busca e a altura calculada sem recursão (BFS com pares `(nó, nível)`). Resultado: altura 2999 na ABB contra 11 na AVL, e 1521 contra 10,6 nós visitados por busca.
- **Questão 3 — Livro de ofertas de uma corretora:** AVL com preço → quantidade. Implementa registrar oferta, melhor oferta (o nó mais à direita), venda pelos maiores preços e volume em um intervalo de preços com poda, visitando O(k + log n) nós.
- **Questão 4 — Ranking ao vivo de um jogo:** `Placar` com duas AVLs, uma de jogador → pontos e outra com a chave `(-pontos, jogador)`. Cada partida remove a chave antiga do ranking e insere a nova. `top(k)` usa um percurso em-ordem que para cedo. Traz ainda a análise de por que a remoção pode rebalancear vários níveis e a comparação com uma lista ordenada.

## Como executar

**Google Colab:** abra o [Colab](https://colab.research.google.com), vá em *Arquivo → Fazer upload de notebook*, escolha `edbii-pratica-avl.ipynb` e use *Ambiente de execução → Executar tudo*.

**Jupyter local:**

```bash
pip install notebook
jupyter notebook edbii-pratica-avl.ipynb
```

Depois, use *Kernel → Restart & Run All*. O notebook usa só a biblioteca padrão do Python 3.
