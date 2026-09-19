# EP2 — Trie Data Structure Manager 🌳

![Language](https://img.shields.io/badge/language-C-blue?style=flat-square&logo=c)
![Data Structure](https://img.shields.io/badge/data%20structure-Trie-orange?style=flat-square)
![Recursion](https://img.shields.io/badge/technique-Recursion-purple?style=flat-square)
![USP](https://img.shields.io/badge/university-USP-darkgreen?style=flat-square)
![Status](https://img.shields.io/badge/status-completed-brightgreen?style=flat-square)

---

## 🇺🇸 English

### About

This project was developed as **Programming Exercise 2 (EP2)** for the course **ACH2023 — Algorithms and Data Structures I** at the **University of São Paulo (USP)**, 2nd semester of 2024.

The program implements a complete **Trie** (also known as a prefix tree or digital tree) management system in C, supporting word insertion, deletion, and search operations, along with structural counters.

### What is a Trie?

A Trie is a tree-based data structure where each node represents a character. Words are stored along paths from the root to leaf nodes. It is especially efficient for prefix-based operations and is widely used in Natural Language Processing (NLP), autocomplete systems, and dictionaries.

```
        (root)
          |
          d
         / \
        a   e
            |
            d
            |
            o
```
*Example: Trie containing the words "da" and "dedo"*

### Implemented Functions

| Function | Description |
|---|---|
| `inicializar` | Initializes the trie root node |
| `criarNo` | Allocates and initializes a new node |
| `inserir` | Recursively inserts a word into the trie |
| `buscarPalavra` | Returns the number of copies of a word in the trie |
| `excluir` | Removes one copy of a word from the trie |
| `excluirTodas` | Removes all copies of a word and cleans up unused nodes |
| `contarNos` | Recursively counts all nodes in the trie |
| `contarArranjos` | Counts internal (non-leaf) nodes |
| `contarPalavras` | Counts total words, including duplicates |
| `contarPalavrasDiferentes` | Counts unique words |
| `exibir` | Prints all words in alphabetical order |

### How It Works

Each node (`NO`) stores:
- `contador` — how many times the word ending at this node was inserted
- `filhos` — array of 26 pointers (one per lowercase letter a–z), or `NULL` if the node has no children

Memory is allocated lazily: the children array is only created when a node actually needs children, keeping memory usage efficient.

### Requirements

- GCC compiler
- Linux terminal (or Windows CMD)

### How to Compile

```bash
gcc -o ep2 12822076.c
```

### How to Run

```bash
./ep2
```

The `main()` function includes a built-in test suite that exercises all operations: initialization, insertion, search, single deletion, and full deletion.

### Example Operations

```c
inserir(&raiz, "melao", 5);      // inserts "melao"
inserir(&raiz, "melao", 5);      // inserts "melao" again (contador = 2)
buscarPalavra(&raiz, "melao", 5); // returns 2
excluir(&raiz, "melao", 5);      // removes one copy (contador = 1)
excluirTodas(&raiz, "melao", 5); // removes all copies and cleans up nodes
```

### Project Structure

```
12822076.c   ← main source file
README.md    ← this file
```

---

## 🇧🇷 Português

### Sobre

Este projeto foi desenvolvido como **Exercício de Programação 2 (EP2)** da disciplina **ACH2023 — Algoritmos e Estruturas de Dados I** da **Universidade de São Paulo (USP)**, 2º semestre de 2024.

O programa implementa um sistema completo de gerenciamento de **Trie** (também conhecida como árvore de prefixos ou árvore digital) em C, com suporte a inserção, exclusão e busca de palavras, além de contadores estruturais.

### O que é uma Trie?

Uma Trie é uma estrutura de dados em árvore onde cada nó representa um caractere. As palavras são armazenadas ao longo dos caminhos da raiz até as folhas. É especialmente eficiente para operações baseadas em prefixos e muito utilizada em Processamento de Linguagem Natural (PLN), sistemas de autocomplete e dicionários.

```
        (raiz)
          |
          d
         / \
        a   e
            |
            d
            |
            o
```
*Exemplo: Trie contendo as palavras "da" e "dedo"*

### Funções Implementadas

| Função | Descrição |
|---|---|
| `inicializar` | Inicializa o nó raiz da trie |
| `criarNo` | Aloca e inicializa um novo nó |
| `inserir` | Insere uma palavra na trie recursivamente |
| `buscarPalavra` | Retorna o número de cópias de uma palavra na trie |
| `excluir` | Remove uma cópia de uma palavra da trie |
| `excluirTodas` | Remove todas as cópias de uma palavra e limpa nós desnecessários |
| `contarNos` | Conta recursivamente todos os nós da trie |
| `contarArranjos` | Conta os nós internos (que possuem filhos) |
| `contarPalavras` | Conta o total de palavras, incluindo duplicatas |
| `contarPalavrasDiferentes` | Conta apenas palavras únicas |
| `exibir` | Imprime todas as palavras em ordem alfabética |

### Como Funciona

Cada nó (`NO`) armazena:
- `contador` — quantas vezes a palavra que termina neste nó foi inserida
- `filhos` — arranjo de 26 ponteiros (um por letra minúscula de a–z), ou `NULL` se o nó não tiver filhos

A memória é alocada de forma lazy: o arranjo de filhos só é criado quando o nó efetivamente precisar de filhos, mantendo o uso de memória eficiente.

### Requisitos

- Compilador GCC
- Terminal Linux (ou CMD do Windows)

### Como Compilar

```bash
gcc -o ep2 12822076.c
```

### Como Executar

```bash
./ep2
```

A função `main()` inclui uma suíte de testes que exercita todas as operações: inicialização, inserção, busca, exclusão simples e exclusão total.

### Exemplo de Operações

```c
inserir(&raiz, "melao", 5);       // insere "melao"
inserir(&raiz, "melao", 5);       // insere "melao" novamente (contador = 2)
buscarPalavra(&raiz, "melao", 5); // retorna 2
excluir(&raiz, "melao", 5);       // remove uma cópia (contador = 1)
excluirTodas(&raiz, "melao", 5);  // remove todas as cópias e limpa os nós
```

### Estrutura do Projeto

```
12822076.c   ← arquivo fonte principal
README.md    ← este arquivo
```

---

*Developed by Luiza de Jesus Lopes — USP nº 12822076*
