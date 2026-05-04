📌 Descrição do Projeto

Este projeto consiste em uma aplicação de lista de tarefas (To-Do List) desenvolvida com JavaScript puro, que permite ao usuário adicionar, visualizar, marcar como concluídas e remover tarefas de forma dinâmica.

A aplicação utiliza manipulação do DOM para atualizar a interface em tempo real, sem necessidade de recarregar a página.

⚙️ Como funciona
1. Adição de tarefas

O usuário digita uma tarefa em um campo de entrada e clica em um botão (ou pressiona Enter).
O JavaScript captura esse valor e cria um novo elemento na lista.

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
2. Manipulação do DOM

O JavaScript interage diretamente com o HTML usando métodos como:

getElementById
createElement
appendChild
addEventListener

Isso permite criar, alterar e remover elementos dinamicamente.

3. Marcar tarefa como concluída

Ao clicar em uma tarefa, ela pode ser marcada como concluída (geralmente com um risco no texto).

li.addEventListener("click", () => {
  li.classList.toggle("concluida");
});
4. Remoção de tarefas

Cada tarefa pode ter um botão de exclusão.

const btnRemover = document.createElement("button");
btnRemover.textContent = "Remover";

btnRemover.addEventListener("click", () => {
  li.remove();
});

li.appendChild(btnRemover);
5. Persistência de dados (opcional, mas importante)

Para salvar as tarefas mesmo após atualizar a página, utiliza-se o Local Storage:

localStorage.setItem("tarefas", JSON.stringify(listaDeTarefas));

E para recuperar:

const tarefas = JSON.parse(localStorage.getItem("tarefas"));
🚀 Funcionalidades
✅ Adicionar tarefas
✅ Marcar como concluída
✅ Remover tarefas
✅ Armazenamento local (Local Storage)
✅ Interface dinâmica sem recarregamento
🧠 Conceitos utilizados
Manipulação do DOM
Eventos (Event Listeners)
Estruturas de dados (arrays/objetos)
JSON (para armazenamento)
Local Storage
📦 Tecnologias
HTML5
CSS3
JavaScript (Vanilla JS)
