<template>
    <div>
        <div class="quote col-md-3" v-for="quote in quotes">
            {{ quote }}
        </div>
    </div>
</template>

<script>
    export default {
        props: ["quotes"]
    }
</script>

<style>
    .quote {
        border: 1px solid #f5f6fa;
        height: 100px;
        text-align: center;
        font-family: "Arizonia";
        font-size: 24px;
        color: #7f8c8d;
        border-radius: 5px;
        margin: 10px;
        padding-top: 20px;
    }
</style>