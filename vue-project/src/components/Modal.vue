<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal">
            <h1>{{header}}</h1>
            <p>{{ text }}</p>
        </div>
    </div>
   
</template>

<script>
export default {
    props: ['header', 'text', 'theme'],
    methods: {
        closeModal() {
            this.$emit('close')
        }
    }
    }
</script>

<style scoped>
.modal{
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: white;
    border-radius: 10px;
}

.backdrop{
    top: 0;
    position: fixed;
    background: rgb(0,0,0,0.5);
    width: 100%;
    height: 100%;
}
h1, p{
    text-align: center;
    color: rgb(4, 149, 149);
}
</style>