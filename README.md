# 🧠 Desafios de Lógica em JavaScript

Coleção de exercícios práticos em JavaScript desenvolvidos durante meus estudos, focados em **condicionais**, **funções** e **métodos de array** (`includes`, `find` e `filter`).

![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-executável-339933?logo=node.js&logoColor=white)
![Status](https://img.shields.io/badge/status-em%20estudo-blue)

---

## 📋 Sumário

- [Sobre o projeto](#-sobre-o-projeto)
- [Desafios](#-desafios)
- [Conceitos praticados](#-conceitos-praticados)
- [Como executar](#-como-executar)
- [Próximos passos](#-próximos-passos)
- [Autor](#-autor)

---

## 📖 Sobre o projeto

Este repositório reúne pequenos desafios de programação resolvidos em JavaScript puro, sem bibliotecas externas. O objetivo é consolidar os fundamentos da linguagem e praticar a resolução de problemas do dia a dia de uma pessoa desenvolvedora.

---

## 🎯 Desafios

### 1. Verificador de número negativo, positivo ou zero

Função que recebe um número e retorna uma string indicando se ele é **negativo**, **positivo** ou **zero**.

```javascript
function checkNumber(num) {
  if (num < 0) {
    return 'Negativo';
  } else if (num > 0) {
    return 'Positivo';
  } else {
    return 'Zero';
  }
}

console.log(checkNumber(-20)); // Negativo
console.log(checkNumber(40));  // Positivo
console.log(checkNumber(0));   // Zero
```

**Conceitos:** funções, estruturas condicionais (`if / else if / else`), operadores de comparação.

---

### 2. Verificação de elemento em um array

Função que recebe um array de números e um valor, e informa se esse valor existe dentro do array.

```javascript
function containsValue(array, value) {
  return array.includes(value);
}

const lista = [1, 2, 3, 4, 5];

console.log(containsValue(lista, 3)); // true
console.log(containsValue(lista, 6)); // false
```

**Conceitos:** parâmetros, retorno de valores booleanos, método `Array.prototype.includes()`.

---

### 3. Buscar produto com preço igual a R$ 20

Dado um array de objetos, encontrar o produto cujo preço seja exatamente R$ 20.

```javascript
const products = [
  { name: 'Maçã', price: 2.5 },
  { name: 'Coca-Cola', price: 8 },
  { name: 'Guaraná', price: 5 },
  { name: 'Chocolate', price: 20 }
];

const checkProduct = products.find((product) => product.price === 20);

console.log(checkProduct); // { name: 'Chocolate', price: 20 }
```

> O método `find()` retorna o **primeiro** elemento que satisfaz a condição, ou `undefined` caso nenhum seja encontrado (ex.: ao buscar `price === 70`).

**Conceitos:** arrays de objetos, arrow functions, `Array.prototype.find()`.

---

### 4. Filtrar produtos com preço menor que R$ 8

Utilizando o mesmo array de produtos, retornar todos os itens com preço inferior a R$ 8.

```javascript
const cheapProducts = products.filter((product) => product.price < 8);

console.log(cheapProducts);
// [ { name: 'Maçã', price: 2.5 }, { name: 'Guaraná', price: 5 } ]
```

> O método `filter()` retorna um **novo array** com todos os elementos que atendem à condição, sem alterar o original.

**Conceitos:** `Array.prototype.filter()`, imutabilidade, arrow functions.

---

## 🛠️ Conceitos praticados

| Conceito | Onde foi aplicado |
| --- | --- |
| Funções e parâmetros | Desafios 1 e 2 |
| Condicionais (`if / else`) | Desafio 1 |
| Operadores de comparação | Desafios 1, 3 e 4 |
| `Array.includes()` | Desafio 2 |
| `Array.find()` | Desafio 3 |
| `Array.filter()` | Desafio 4 |
| Arrow functions | Desafios 3 e 4 |
| Array de objetos | Desafios 3 e 4 |

---

## 🚀 Como executar

**Pré-requisito:** [Node.js](https://nodejs.org/) instalado.

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/nome-do-repositorio.git

# Acesse a pasta do projeto
cd nome-do-repositorio

# Execute o arquivo
node index.js
```

Também é possível testar os códigos diretamente no console do navegador (`F12` → aba **Console**).

---

## 🔮 Próximos passos

- [ ] Adicionar tratamento de erros (ex.: validar se o parâmetro é realmente um número)
- [ ] Criar testes automatizados com Jest
- [ ] Praticar outros métodos de array: `map`, `reduce`, `some` e `every`
- [ ] Organizar cada desafio em um arquivo separado

---

## 👤 Autor

**Seu Nome**

[![GitHub](https://img.shields.io/badge/GitHub-seu--usuario-181717?logo=github)](https://github.com/seu-usuario)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-seu--perfil-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/seu-perfil)

---

⭐ Se este repositório te ajudou de alguma forma, deixe uma estrela!
