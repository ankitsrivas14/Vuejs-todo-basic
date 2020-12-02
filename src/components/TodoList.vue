<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <p class="display-3">Vue Basic Todo App</p>
            </div>
        </div>
        <div class="row">
            <p>Add create form</p>
        </div>
        <div class="row">
            <div class="col-12 col-lg-6">
                <u class="list-group">
                    <Todo v-for="(todo,index) in todos" 
                        :key="index" 
                        :todo="todo.todoString"
                        :completed="todo.completed"
                    />
                </u>
            </div>
        </div>
    </div>
</template>

<script>
import Todo from "./Todo"
export default {
    components:{
        Todo
    },
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