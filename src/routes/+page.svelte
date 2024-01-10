<script>
    import TodoList from "$lib/TodoList.svelte";

    import {v4 as uuid} from "uuid";

    const todos = [
        {
            id: uuid(),
            title: "Todos item one",
            completed: true
        },
        {
            id: uuid(),
            title: "Todos item two",
            completed: false
        },
        {
            id: uuid(),
            title: "Todos item three",
            completed: true
        },        {
            id: uuid(),
            title: "Todos item four thousand shillings!",
            completed: true
        },
    ]
</script>

<TodoList todos={todos}></TodoList>