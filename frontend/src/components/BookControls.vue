<template>
    <div>
        <b-button pill @click="sortByAuthor">Ordenar por Autor</b-button>
        <b-button pill @click="sortByDate">Ordenar por fecha</b-button>
        <b-button pill @click="insert">Agregar nuevo libro</b-button>
        <b-button pill @dragover.prevent @drop="edit">Editar</b-button>
        <b-button pill @dragover.prevent @drop="deleteBook">Eliminar</b-button>
    </div>
</template>

<script>
    export default{
        methods:{
            sortByAuthor(){
                this.$emit('sortByAuthor');
            },
            sortByDate(){
                this.$emit('sortByDate');
            },
            insert(){
                this.$emit('insert');
            },
            edit(){
                this.$emit('edit');
            },
            deleteBook(){
                this.$emit('deleteBook')
            }
        }
    }
</script>