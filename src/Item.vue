<template>
    <div class="item">
        {{ name }}
        <input type="text">
        <button @click="taskStatus()">New Bill</button>
    </div>


</template>

<script>
export default {
    name: 'item',

    data(){
        return{
            name: button
        }
        
    },
    methods: {
        taskStatus: function (){
            alert("tarefa completa");
        }
    }
}

</script>
<style>
/* .dashboard {
    padding: 5px;
    margin: 0 auto;
    min-height: 40px;
    width: 70vw;
    height: 50vw;
    box-shadow: 0 0 10px rgb(0, 0, 0);
    text-transform: uppercase;
    text-align: center;
} */
</style>


