<template>
    <div class="container">
        <quote-grid></quote-grid>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';

    export default {
        data () {
            return {
              maxQuotes: 10,
              quotes: ['Hey!']  
            }
        },
        components: {
            'quote-grid': QuoteGrid
        }
    }
</script>

<style>
</style>
