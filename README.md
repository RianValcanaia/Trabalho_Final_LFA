<div align="center" id="topo">

<img src="https://media.giphy.com/media/iIqmM5tTjmpOB9mpbn/giphy.gif" width="200px" alt="Gif animado"/>

# <code><strong> Simulador de Torre de Hanoi com Autômato com Pilha </strong></code>

<em>Implementação do problema da Torre de Hanoi utilizando um Autômato com Pilha como mecanismo de evolução.</em>

[![Python Usage](https://img.shields.io/badge/Python-100%25-blue?style=for-the-badge&logo=python)]()
[![Status](https://img.shields.io/badge/Status-Concluído-green?style=for-the-badge)]()
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Visite%20meu%20perfil-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/rian-carlos-valcanaia-b2b487168/)

</div>

## Índice

- [📌 Objetivos](#-objetivos)
- [📥 Entradas do sistema](#-entradas-do-sistema)
- [🧱 Estruturas de Dados](#-estruturas-de-dados)
- [🧰 Funcionalidades](#-funcionalidades)
- [📊 Exemplo de Execução](#-exemplo-de-execução)
- [📂 Como executar](#-como-executar)
- [👨‍🏫 Envolvidos](#-envolvidos)
- [📅 Curso](#-curso)
- [📄 Código-fonte](#-código-fonte)

## 📌 Objetivos

*   Simular a resolução do problema clássico da Torre de Hanoi.
*   Modelar a solução utilizando um Autômato de Pilha (AP).
*   Demonstrar o funcionamento do AP, exibindo o estado da pilha e a configuração das torres a cada passo da execução.
*   Diferenciar as transições internas do autômato (expansão e simplificação de regras) dos movimentos de disco.

[⬆ Voltar ao topo](#topo)

## 📥 Entradas do sistema

*   O usuário deve fornecer o **número de discos** (um número inteiro maior ou igual a 1) que serão utilizados na simulação da Torre de Hanoi.

[⬆ Voltar ao topo](#topo)

## 🧱 Estruturas de Dados

### 🔸 `Pilha`

Classe que implementa a estrutura de dados de Pilha (LIFO) para o autômato.

```python
class Pilha:
    def __init__(self):
        self.itens = ['#']
    def empilhar(self, item):
    def desempilhar(self):
    def vazia(self):
    def mostrar(self):
```

### 🔸 `AutomatoPilha`

Classe principal que representa o Autômato de Pilha e contém toda a lógica da simulação da Torre de Hanoi.
```python
class AutomatoPilha:
    def __init__(self, n_discos, origem='A', destino='C'):
        self.estado_atual = "q0"
        self.n_discos = n_discos
        self.pilha = Pilha()
        self.torres = {
            'A': list(range(n_discos, 0, -1)),
            'B': [],
            'C': []
        }
    def executar(self):
```

[⬆ Voltar ao topo](#topo)

## 🧰 Funcionalidades

### 🔹 Funções Principais

*   `AutomatoPilha.executar()` : Inicia e controla a simulação. Executa um loop que desempilha e processa símbolos até que a pilha contenha apenas o marcador de base `#`, finalizando a solução do problema.

### 🔸 Funções Secundárias

*   **Classe `Pilha`**:
    *   `empilhar()`: Adiciona um item ao topo da pilha.
    *   `desempilhar()`: Remove e retorna o item do topo da pilha.
    *   `vazia()`: Verifica se a pilha está vazia.
    *   `mostrar()`: Retorna uma representação em string do conteúdo da pilha.
*   **Classe `AutomatoPilha`**:
    *   `_obter_torre_auxiliar()`: Calcula qual das três torres ('A', 'B', 'C') é a auxiliar, dadas a origem e o destino.
    *   `_imprimir_passo()`: Exibe o estado atual da simulação, incluindo a transição realizada, o conteúdo da pilha e a disposição dos discos nas torres.

[⬆ Voltar ao topo](#topo)

## 📊 Exemplo de Execução

1.  O usuário executa o script Python.
2.  O sistema solicita a entrada do número de discos.
3.  Após a entrada do usuário, o autômato é inicializado com o problema `h(n, A, C)` na pilha.
4.  A cada passo, o programa imprime na tela a transição formal do autômato, o estado atual da pilha e a configuração das torres (A, B, C).
5. Ao final, o programa exibe o número total de movimentos de disco realizados para resolver o problema.

[⬆ Voltar ao topo](#topo)

## 📂 Como executar

Para executar o programa, você precisa ter o Python instalado. Abra um terminal no diretório do arquivo e execute o seguinte comando:

```bash
python3 main.py
```

O programa então solicitará que você digite o número de discos.

[⬆ Voltar ao topo](#topo)

## 👨‍🏫 Envolvidos

*   **Professor**: Ricardo Ferreira Martins
*   **Estudantes**:
    * Camile Neves
    *   [Rian Carlos Valcanaia](https://github.com/RianValcanaia)

[⬆ Voltar ao topo](#topo)

## 📅 Curso

*   **Universidade**: Universidade do Estado de Santa Catarina (UDESC)
*   **Disciplina**: Linguagens Formais e Autômatos
*   **Semestre**: 4º

[⬆ Voltar ao topo](#topo)

## 📄 Código-fonte

🔗 [https://github.com/RianValcanaia/LFA_Torre_de_Hanoi_com_AP](https://github.com/RianValcanaia/LFA_Torre_de_Hanoi_com_AP)

[⬆ Voltar ao topo](#topo)
