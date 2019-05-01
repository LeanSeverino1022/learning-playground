<template>
    <div>
        <h1>Todos</h1>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoItem v-on:del-todo="$emit('del-todo', todo.id)" v-bind:todo ="todo"/>
        </div>    
    </div>
</template>
<script>

import TodoItem from './TodoItem.vue';

export default {
    name: 'Todos',
    components: {
        TodoItem
    },
    methods: {
        test: function(){ console.log('called 123')}
    },
    props: ['todos']
}
</script>

<style scoped>

</style>

// TODO
// learn modules for es6 again
