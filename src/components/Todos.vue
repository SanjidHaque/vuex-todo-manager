<template>
    <div>
        <div class="row" style="padding-top: 20px; text-align: left; font-weight: bold;">
            <div class="col-12">
                Todo Manager
            </div>
        </div>

        <div class="row">
            <div class="col-4 todo" v-for="todo in allTodos" v-bind:key="todo.id">
                {{ todo.title }}
            </div>
        </div>


    </div>
</template>

<script>
    import {mapGetters, mapActions} from 'vuex';

    export default {
        name: 'Todos',
        components: {

        },
        methods: {
            ...mapActions(['fetchTodos'])
        },
        computed: mapGetters(['allTodos']),
        created() {
            this.fetchTodos();
        }
    }
</script>

<style scoped>
    .todo {
        border: 1px solid #ccc;
        padding: 20px;
        background: #41b883;
        border-radius: 5px;
        text-align: center;
        cursor: pointer;
        font-weight: bold;
    }
</style>
