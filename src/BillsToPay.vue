<template>
    <div class="bills-to-pay">
        <p>Paid Bills: {{ bills.filter(bill => {return bill.paid === true}).length }}</p>
        <p>Pending Bills: {{ bills.filter(bill => {return bill.paid === false}).length }}</p>
        <bill v-for="bill in bills" :bill="bill" :key="bill.id"/>
    </div>

</template>

<script>
import Bill from "./Bill"

export default {
    name: 'billsToPay',
    props: ['bills'],
    components: {
        Bill,
    },
    data(){
        return{
            
        }
        
    },
    methods: {
        changeStatus: function(){
            
        }
    }
}

</script>
<style>
.dashboard {
    padding: 5px;
    margin: 0 auto;
    min-height: 40px;
    width: 70vw;
    height: 50vw;
    box-shadow: 0 0 10px rgb(0, 0, 0);
    text-transform: uppercase;
    text-align: center;
    
}
</style>


