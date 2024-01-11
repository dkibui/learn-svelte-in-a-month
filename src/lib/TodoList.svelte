<script>
    import Button from "$lib/Button.svelte";
    import {v4 as uuid} from "uuid";

    export let todos = [];
    let inputText = "";

    const handleAddTodo = () => {
        if (!inputText) return;
        todos = [...todos, {
            id: uuid(),
            title: inputText,
            completed: false
        }]
        inputText = "";
    }
</script>

<h2>Todos</h2>

<div class="todo-list-wrapper">
    <ul>
        {#if todos}
            {#each todos as {id, title}, index (id)}
                <li>{title}</li>
            {/each}
        {:else }
            <li>There are no todos!</li>
        {/if}
    </ul>
    <p>{inputText}</p>
    <form class="add-todo-form" on:submit|preventDefault={handleAddTodo}>
        <input type="text" bind:value={inputText}>
        <Button type="submit" disabled={!inputText}>Add</Button>
    </form>
</div>