<template>
    <div class="container">
        <new-quote @addQuote="addQuote"></new-quote>
        <quotes :quotes="quotes"></quotes>
    </div>
</template>

<script>
    import NewQuote from "./NewQuote.vue";
    import Quotes from "./Quotes.vue";

    export default {
        data: function() {
            return {
                quotes: ["My First quote"],
                maxQuotes: 10
            }
        },
        methods: {
            addQuote(quote) {
                console.log((this.quotes).length);
                if(this.quotes.length < this.maxQuotes) {
                    this.quotes.push(quote);
                }
            }
        },
        components: {
             'new-quote': NewQuote,
             quotes: Quotes 
        }
    }
</script>

<style>
</style>
