<template>
    <div id="heading">
        <p>Rank</p>
        <p>Name</p>
        <p>Net Worth</p>
        <p>Age</p>
        <p>Source</p>
        <p>Country</p>
    </div>
    <div v-for="billionaire of billionaires" :key="billionaire.rank">
        <BillionairesItem :billionaire=billionaire />
    </div>
</template>

<script>
    import BillionairesItem from './BillionairesItem.vue'
    export default{
        name: 'BillionairesList',
        props:{
            billionaires: Array
        },
        components:{
            BillionairesItem
        }
    }
</script>

<style scoped>
    #heading {
        background-color: #333;
        color: #ffffff;
        display: flex;
    }
    p {
        flex: 1;
        font-size: 20px; 
    }
    @media only screen and (max-width: 500px) { 
        p {
            font-size: 16px; 
        }
    }
</style>