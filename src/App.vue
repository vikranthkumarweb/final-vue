<template>
  <!-- Step 3: use the component -->
  <BillionairesHeader title="Billionaires Index" />
  <BillionairesList :billionaires=billionaires />
</template>

<script>
    // Step 1 : you import the component
    import BillionairesHeader from './components/BillionairesHeader.vue'
    import BillionairesList from './components/BillionairesList.vue'

    export default{
      name: 'App',
      // Step 2: register the component
      components:{
        BillionairesHeader,
        BillionairesList 
      },
      data(){
        return {
          billionaires: []
        }
      },
      methods:{
        async fetchBillionaires(){
          const res = await fetch("https://final-node-oypw.onrender.com/api")
          const data = await res.json()
          console.log(data)
          return data[0].billionaires
        }
      },
      async created(){
        this.billionaires = await this.fetchBillionaires()
      }
    }
</script>

<style>
    body {
        background-color: #f7f7f7;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        margin: 0px;
        text-align: center;
    }
</style>