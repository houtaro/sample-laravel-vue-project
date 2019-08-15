<template>
    <div>
        
    </div>
</template>

<script>
export default {
    name: "AddTodo",
    data() {
        return {
            form: {
                todos: []
            }
        }
    },
    methods: {
        save() {
            let vm = this;
            vm.form.todos.push(form.todo);
            alert("Saved!");
        }
    }    
}
</script>

<style scoped>

</style>