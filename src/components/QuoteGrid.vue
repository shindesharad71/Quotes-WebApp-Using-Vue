<template>
    <div class="row">
        <p v-for="quote in quotes">{{quote}}</p>
    </div>
</template>

<script>
export default {
    props: ['quotes']
}
</script>

<style scoped>

</style>

