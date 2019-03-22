<template>
    <div>
        <h2>Quotes</h2>
        <div class="container">
            <div class="progress">
                <div class="progress-bar" role="progressbar" aria-valuenow="totalQuotes" aria-valuemin="0" aria-valuemax="100" :style="{width: (total) + '%'}">
                    {{ total }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props:["totalQuotes"],
        computed: {
            total() {
                return this.totalQuotes * 10;
            }
        }
        
    }
</script>

<style scoped>
    h2 {
        text-align: center
    }
    .container {
        display: flex;
        justify-content: center;
        margin: 20px;
    }
    .progress {
        width: 50%;
    }
</style>
