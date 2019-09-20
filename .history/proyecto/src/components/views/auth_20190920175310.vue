<template>
    <div id="auth">
        <h1>Autentificado/a</h1>
    </div>
</template>

<script>
    export default {
        name: 'Auth',
        data() {
            return {
                 input: {
                    username: '',
                    password: ''
                }
            }
        }
    }
</script>

<style scoped>
    #secure {
        background-color: #FFFFFF;
        border: 1px solid #CCCCCC;
        padding: 20px;
        margin-top: 10px;
    }
</style>