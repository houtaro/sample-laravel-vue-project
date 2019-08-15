<template>
    <div>
        <h1>Todo List: </h1>
        <div class="item" v-for="todoitem in form.todos" :key="todoitem.id">
            <h3> {{ todoitem.title }} </h3>
            <small>{{ todoitem.desc }}</small>
        </div>

        <table>
            <tr>
                <td>ID: </td>
                <td>
                    <input type="text" name="todo"  id="todo" v-model="form.todo_id"> 
                </td>
            </tr>
            <tr>
                <td>Title: </td>
                <td>
                    <input type="text" name="todo"  id="todo" v-model="form.todo_title">
                </td>
            </tr>
            <tr>
                <td>
                    Description:
                </td>
                <td>
                    <input type="text" name="todo"  id="todo" v-model="form.todo_desc">
                </td>
            </tr>
        </table>

        <button @click="save" class="btn btn-primary">Add</button>
    </div>
</template>

<script>
export default {
    name: 'TodoList',
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
            vm.form.todos.push({
                id: vm.form.todo_id,
                title: vm.form.todo_title,
                desc: vm.form.todo_desc
            });
        }
    }
}
</script>

<style scoped>
    .item {
        padding: 10px;
        background-color: #f4f4f4;
        border-bottom: 1px #ccc solid;
    }

    .is-completed {
        text-decoration: line-through;
    }
</style>