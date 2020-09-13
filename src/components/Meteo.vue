<template>


<div class="container">
<h1 class="my-4">App Meteo avec Vue.js</h1>
<div class="form-group">
    <label for="position">Entrez le nom d'une ville</label>
    <input type="text" id="position" class="form-control" v-model="requete" @keypress="goMeteo">
</div>

<div class="w-75 m-auto" v-if="temps">
    <h3 class="text-center mb-3">Position : {{temps.name}}</h3>
    <div class="card text-center p-5">
        <p class="texte-affichage">
            Temprérature : {{temps.main.temp.toFixed()}}
        </p>
        <p class="texte-affichage">
            Temps : {{temps.weather[0].description}}
        </p>
    </div>
</div>
</div>
    

</template>





<script>

import axios from "axios"


export default {

    name: "Meteo",
    data(){
        return {
            requete: "",
            temps: undefined,
            apiCode: "2dce2d135bf36620109ad59883999ad4",
            urlRecherche: "https://api.openweathermap.org/data/2.5/weather?"

        }
    },
    methods: {
        goMeteo(e){
            if(e.key == "Enter") {
                axios
                .get(`${this.urlRecherche}q=${this.requete}&units=metric&APPID=${this.apiCode}&lang=fr`)
                .then(response => {
                    this.temps = response.data
                })
                this.requete = ""
            }

        }
    }

    
}


</script>




<style>

.texte-affichage {
    font-size: 30px;
    font-weight: 300;
    line-height: 1.2;
}

</style>