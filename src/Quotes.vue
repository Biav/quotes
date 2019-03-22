<template>
    <div>
        <div class="quote col-md-3" v-for="(quote, key) in quotes" @click="deleteQuote(key)">
            <span class="glyphicon glyphicon-remove" aria-hidden="true"></span>
            {{ quote }}
        </div>
    </div>
</template>

<script>
    export default {
        props: ["quotes"],
        methods: {
            deleteQuote(index) {
                this.$emit("deleteQuote", index);
            }
        }
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

    .quote:hover{
        background: #e74c3c;
    }

    span {
        color: #ffffff;
        font-size: 10px;
        float: right;
        margin-top: -10px;
    }
</style>