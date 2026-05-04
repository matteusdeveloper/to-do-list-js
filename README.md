# 📌 To-Do List em JavaScript

Uma aplicação simples de lista de tarefas (**To-Do List**) desenvolvida com **JavaScript puro (Vanilla JS)**, permitindo adicionar, concluir e remover tarefas de forma dinâmica, sem recarregar a página.

---

## 🚀 Funcionalidades

* Adicionar novas tarefas
* Marcar tarefas como concluídas
* Remover tarefas
* Atualização dinâmica da interface
* Armazenamento local com Local Storage

---

## ⚙️ Como funciona

### ➕ Adicionar tarefas

O usuário digita uma tarefa em um campo de entrada e a adiciona à lista.
O JavaScript cria dinamicamente um novo elemento HTML.

```javascript
function adicionarTarefa() {
  const input = document.getElementById("input-tarefa");
  const texto = input.value;

  if (texto.trim() !== "") {
    const li = document.createElement("li");
    li.textContent = texto;

    document.getElementById("lista").appendChild(li);
    input.value = "";
  }
}
```

---

### 🧠 Manipulação do DOM

A aplicação utiliza métodos como:

* `getElementById`
* `createElement`
* `appendChild`
* `addEventListener`

Para atualizar a interface em tempo real.

---

### ✔️ Marcar como concluída

```javascript
li.addEventListener("click", () => {
  li.classList.toggle("concluida");
});
```

---

### 🗑️ Remover tarefas

```javascript
const btnRemover = document.createElement("button");
btnRemover.textContent = "Remover";

btnRemover.addEventListener("click", () => {
  li.remove();
});

li.appendChild(btnRemover);
```

---

### 💾 Persistência com Local Storage

```javascript
localStorage.setItem("tarefas", JSON.stringify(listaDeTarefas));
```

```javascript
const tarefas = JSON.parse(localStorage.getItem("tarefas"));
```

---

## 🧠 Conceitos utilizados

* Manipulação do DOM
* Eventos (Event Listeners)
* Arrays e Objetos
* JSON
* Local Storage

---

## 🛠️ Tecnologias

* HTML5
* CSS3
* JavaScript

---

## 📷 Preview

*(adicione aqui um print do projeto depois)*

---

## 📄 Licença

Este projeto está sob a licença MIT.
