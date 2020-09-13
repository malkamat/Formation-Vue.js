<template>
    <div class="header-top"><p>TP : To-Do Liste</p></div>
</template>


<script>



export default {
    name: "Header",
    data(){
        return {
            titre: "Mon titre de base"
        }

    }
}
</script>

<style scoped>

.header-top {
    position: fixed;
    top: 0;
    height: 50px;
    background: #333333;
    color: #f1f1f1;
    width: 100%;
    text-align: center;
    line-height: 50px;
    font-size: 25px;

}



</style>