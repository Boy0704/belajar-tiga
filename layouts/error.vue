<template>

    <div id="tengah">
        <h1 v-if="error.statusCode === 404">PAGE NOT FOUND</h1>
        <h1 v-else>An error occured</h1>
        <a href="javascript:void(0)" @click="$router.push({ path:'/' })"> Back To Home </a>
    </div>

</template>

<style>
    #tengah{
        text-align: center;
    }
</style>

<script>
    export default {

        props: ['error'],
        layout: 'success'


    }
</script>