<template>
  <div id="app">
    <img src="./assets/logo.png">
    <bills-to-pay :bills="bills"/>
  </div>
</template>

<script>
import BillsToPay from './BillsToPay';
import item from './Item';
export default {
  name: 'app',
  components: {
    BillsToPay,
  },
  data () {
    return {
      bills: [{
        id: 1,
        title: 'Phone Bill',
        value: '100,00',
        paid: true
      },{
        id: 2,
        title: 'Rent',
        value: '1200,00',
        paid: false
      },{
        id: 3,
        title: 'Car Maintnance',
        value: '255,00',
        paid: false
      },{
        id: 4,
        title: 'Macbook Pro',
        value: '3899,90',
        paid: false
      }]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

/* ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
} */

a {
  color: #42b983;
}
</style>
