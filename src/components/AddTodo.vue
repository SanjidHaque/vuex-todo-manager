<template>
    <div>
        <div class="row" style="font-weight: bold;">
            <div class="col-xl-12">
                Add Todo
            </div>
        </div>
        <div class="row">
            <div class="col-xl-12">
                <form class="form-group" @submit.prevent="onSubmit">

                    <div class="row">
                        <div class="col-10">
                            <input class="form-control"
                                   type="text"
                                   v-model="title"
                                   placeholder="Add Todo...">
                        </div>

                        <div class="col-2">
                            <input
                                    style="background: #41b883;
                                    color: white;
                                    font-weight: bold;"
                                    class="form-control"
                                    type="submit"
                                    value="Submit">
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    import { mapActions } from 'vuex';
    export default {
        name: 'AddTodo',
        data() {
            return {
                title: ''
            }
        },
        methods: {
            ...mapActions(['addTodo']),
            onSubmit() {
                this.addTodo(this.title)
            }
        }
    }
</script>

<style scoped>

</style>
