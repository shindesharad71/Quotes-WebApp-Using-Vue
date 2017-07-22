<template>
    <div class="container">
        <app-header></app-header>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
        <div class="col-sm-12 text-center">
            <div class="alert alert-info">info: Click on Quote to Delete it.</div>
        </div>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import NewQuote from './components/NewQuote.vue';
    import Header from './components/Header.vue';

    export default {
        data () {
            return {
              maxQuotes: 10,
              quotes: ['Hey!']  
            }
        },
        components: {
            'quote-grid': QuoteGrid,
            'app-new-quote': NewQuote,
            'app-header': Header
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote);
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        }
    }
</script>

<style>
</style>
