<template>
    <div class="row">
        <form>
            <div class="col-md-offset-3 col-md-6 form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-md-offset-3 col-md-6 form-group">
                <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
import Quote from './Quote.vue';

export default {
    data: function() {
        return {
            quote: ''
        };
    }
}
</script>

<style scoped>

</style>

