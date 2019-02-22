<template>
    <section>
        <h1 class="title_text">{{msg}}</h1>
    </section>
</template>

<script>
export default {
    name: 'Home',
    data () {
        return {
            msg: '首頁資訊'
        }
    }
}
</script>

<style lang="sass" scoped>
    h1
        color: blue
</style>
