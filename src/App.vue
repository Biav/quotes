<template>
    <div class="container">
        <headerQuotes :totalQuotes="totalQuotes()"></headerQuotes>
        <new-quote @addQuote="addQuote"></new-quote>
        <quotes :quotes="quotes" @deleteQuote="deleteQuote"></quotes>
    </div>
</template>

<script>
    import NewQuote from "./NewQuote.vue";
    import Quotes from "./Quotes.vue";
    import Header from "./Header.vue";

    export default {
        data: function() {
            return {
                quotes: ["My First quote"],
                maxQuotes: 10
            }
        },
        methods: {
            addQuote(quote) {
                if(this.totalQuotes() < this.maxQuotes) {
                    this.quotes.push(quote);
                }
            },
            totalQuotes() {
                return this.quotes.length;
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        },
        components: {
             'new-quote': NewQuote,
             quotes: Quotes, 
             headerQuotes: Header 
        }
    }
</script>

<style>
</style>
