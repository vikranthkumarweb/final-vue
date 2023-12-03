<template>
    <div>
        <p>{{billionaire.rank}}</p>
        <p>{{billionaire.name}}</p>
        <p>{{billionaire.net_worth}}</p>
        <p>{{billionaire.age}}</p>
        <p>{{billionaire.source}}</p>
        <p>{{billionaire.country}}</p>
    </div>
</template>

<script>
    export default{
        name: 'BillionairesItem',
        props:{
            billionaire: Object
        }
    } 
</script>

<style scoped>
    div {
        background-color: #ffffff;
        display: flex;
    }
    p {
        flex: 1;
        font-size: 18px; 
    }
    @media only screen and (max-width: 500px) { 
        p {
            font-size: 16px; 
        }
    }
</style>