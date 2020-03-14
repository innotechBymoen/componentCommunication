<template>
    <div v-on:click="updateParent" ><p>CLICK ME!</p></div>
</template>

<script>
export default {
    name: 'Updater',
    methods : {
        updateParent : function() {
            this.$emit('myCustomEvent', "Frodo");
        }
    }
};
</script>

<style scoped>
</style>