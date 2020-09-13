<template>
    <div class="container mt-5">
        <h1>Entre des choses à faire.</h1>

        <form action="">

            <div class="form-group">

                <label for="action">Action</label>
                <input v-model="formData.tache" type="text" id="action" class="form-control">


            </div>

            <button @click.prevent="creationItem" class="btn btn-primary mb-3">Créer une nouvelle tâche</button>

        </form>

        <ul>
            <li :key="index" v-for="(tache , index) in tableauTaches">
                <item :id="index" :tache="tache" :suppression="suppression"></item>
            </li>
        </ul>
     
        </div>
</template>




<script>

import Item from "./Item"


export default {
    name: "Contenu",
    data() {
        return {
           formData: {
               tache: "",

           },
           tableauTaches: ["Javascript", "Vue", "Python", "Node"]
          
        }
    },
    components: {
        "item": Item,

    },
    methods: {
       creationItem: function(){
           if(this.formData.tache !== "") {
               this.tableauTaches.push(this.formData.tache)
           this.formData.tache = ""
           }
           
       },
       suppression: function(e){
           this.tableauTaches.splice(e.target.parentNode.id , 1)
       }

    }, 
   
}



</script>






<style scoped>

h1{
margin-top: 100px!important;
}

ul {
    list-style-type: none;
    padding: 0;
}

</style>