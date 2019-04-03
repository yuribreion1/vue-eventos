<template>
    <div>
        <input :type="this.tipo" :class="this.classe" :id="this.id" v-on:keyup="this.mudou">
    </div>
</template>

<script>
export default {
    props: ['tipo','classe', 'id'],
    data() {
        return {
            valorDaCaixa: ""
        }
    }, 
    methods: {
        mudou: function (evt) {
            if (evt.key == "Enter") {
                this.$emit("digitou", this.valorDaCaixa);
            }
        }
    }
}
</script>

<style>

</style>
