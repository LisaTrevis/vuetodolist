<template>
    <div>
        <form v-on:submit="addTodo">
            <input type="text" v-model="title" name="title" placeholder="Add To Do" />
            <input type="submit" value="Submit" class="btn" />
        </form>
    </div>
</template>

<script>
import uuid from 'uuid';
export default {
    name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addTodo(e) {
            e.preventDefault();
            const newTodo = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            }
            // Send up to parent at this point rather than adding it as an $emit() in the form above as we want to create the items before sending it up.
            this.$emit('add-todo', newTodo);

            this.title = '';
        }
    }
}
</script>

<style scoped>
    form {
        display: flex;
    }
    input[type="text"] {
        flex: 10;
        padding: 5px;
    }
    input[type="submit"] {
        flex: 2;
    }
</style>