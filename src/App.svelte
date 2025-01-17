// App.svelte
<script>
  let todos = [
    { id: 1, text: 'Õpi Svelte', done: false },
    { id: 2, text: 'Arenda lihtne projekt', done: false },
  ];

  function toggleDone(id) {
    todos = todos.map(todo => todo.id === id ? { ...todo, done: !todo.done } : todo);
  }

  function deleteTodo(id) {
    todos = todos.filter(todo => todo.id !== id);
  }

  function addTodo() {
    const text = prompt('Sisesta uus ToDo:');
    if (text) {
      todos = [...todos, { id: Date.now(), text, done: false }];
    }
  }
</script>

<style>
  .todo {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 0.5rem;
    padding: 0.5rem;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  .done {
    text-decoration: line-through;
    color: gray;
  }
  button {
    margin-left: 0.5rem;
  }
</style>

<h1>ToDo Rakendus</h1>

<button on:click={addTodo}>Lisa uus ToDo</button>

{#if todos.length === 0}
  <p>ToDo nimekiri on tühi!</p>
{:else}
  <ul>
    {#each todos as { id, text, done }}
      <li class="todo">
        <span class={done ? 'done' : ''} on:click={() => toggleDone(id)}>{text}</span>
        <button on:click={() => deleteTodo(id)}>Kustuta</button>
      </li>
    {/each}
  </ul>
{/if}
