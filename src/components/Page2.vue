<template>
<div>
        <h1>Voici La page 2</h1>
        <div @click="goDebut" class="btn btn-warning">Retour au début</div>

</div>
</template>


<script>

export default {
    name: "Page2",
    methods: {
        goDebut: function() {
            this.$router.push("/")
        }

    }
}


</script>

<style scoped>

</style>