<template>
    <div>
        <TodoList />
    </div>
</template>

<script>
    import TodoList from "./TodoList";

    export default {
        name: 'App',
        components: {
            TodoList
        },
    }
</script>
