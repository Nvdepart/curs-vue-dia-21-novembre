<template>
    <v-container>
        <v-row>
           
            <v-col cols="6" v-if="enviat==false">
                    <v-text-field
                    label="Nom i cognoms"
                    v-model="nomComplet"
                    ></v-text-field>
                    
                    <v-text-field
                    label="Correu electronic"
                    type="email"
                    v-model="correuElectronic">

                    </v-text-field>
                    <v-checkbox
                        v-model="politicaPrivacitat"
                        label="Acceptes la poitica de privacitat ?"
                        color="red"

                    ></v-checkbox>

                    <v-btn @click="enviar()">Enviar</v-btn>
                    <v-btn @click="netejar()">netejar</v-btn>

            </v-col>
            <v-col cols="6" v-else>
                <h1>Missatge enviat</h1>
            </v-col>
            <v-col cols="6">
                {{nomComplet}}
                <br>
                {{correuElectronic}}
                <br>
                {{politicaPrivacitat}}
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
    export default{
        mounted(){
            this.nomComplet="Jordi"
            this.correuElectronic="jordi@google.com"
            this.politicaPrivacitat=true
        },
     
        data(){
            return {
                nomComplet:"",
                correuElectronic:"",
                politicaPrivacitat:false,
                enviat:false
            }
            
        },
        methods: {
            netejar(){
                this.nomComplet="",
                this.correuElectronic="",
                this.PoliticaPrivacitat="false"
            },
            enviar(){
                console.log("Estic enviant")

                if(this.politicaPrivacitat==true){
                    console.log(this.nomComplet)
                    console.log(this.correuElectronic)
                    console.log(this.politicaPrivacitat)
                    this.enviat=true
}
                
            }
        }
    }
</script>