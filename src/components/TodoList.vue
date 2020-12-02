<template>
    <h1>Hello from Todo list template</h1>
</template>

<script>
export default {
    data(){
        return {
            todos:[
                {todoString: "Complete Vue Course", completed:false},
                {todoString: "Order food", completed:true},
                {todoString: "Send documents", completed:false},
                {todoString: "Study CSS animations", completed:true},
                {todoString: "Recharge mobile", completed:false}
            ]
        }
    },
    methods:{
        addTodo(newTodo){
            this.todos.push(
                {todoString:newTodo,completed:false}
            )
        },
        toggleTodo(todo){
            todo.completed = !todo.completed
        },
        editTodo(todo,newTodoString){
            todo.todoString = newTodoString
        },
        deleteTodo(deleteTodo){
            this.todos = this.todos.filter(todo => todo.todoString !== deleteTodo.todoString)
        }
    }
}
</script>

<style>

</style>