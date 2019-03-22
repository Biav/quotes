<template>
    <div class="container">
        <new-quote @addQuote="addQuote"></new-quote>
    </div>
</template>

<script>
    import NewQuote from "./NewQuote.vue";

    export default {
        data: function() {
            return {
                quotes: ["My First quote"]
            }
        },
        methods: {
            addQuote(quote) {
                this.quotes.push(quote);
            }
        },
        components: {
             'new-quote': NewQuote 
        }
    }
</script>

<style>
</style>
