<template>
    <div>
        <p> {{title}}</p>
    </div>
</template>

<script>
    export default{
        name: 'BillionairesHeader',
        props:{
            title: String
        }
    }
</script>

<style scoped>
    p {
        font-size: 30px;
    }
    @media only screen and (max-width: 500px) { 
        p {
            font-size: 25px; 
        }
    }
</style>
