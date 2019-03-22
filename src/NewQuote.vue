<template>
    <div>
        <form class="form-group">

            <textarea class="col-md-6" v-model="quote">
            </textarea>

            <button class="btn btn-primary col-md-6" @click.prevent="addQuote">
                Add quote
            </button>
        </form>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                quote: ''
            }
        },
        methods: {
            addQuote() {
                this.$emit("addQuote", this.quote);
                this.quote = '';
            }
        }
    }
</script>

<style scoped>
    form {
        display: flex;
        align-items: center;
        flex-flow: column;
        margin-top: 20px;
    }

    textarea {
        height: 100px;
        resize: none;
    }
</style>
