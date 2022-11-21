<template>
    <div>

        <v-text-field
            label="Escrui el teu nom"    
            v-model="nom"
            placeholder="p.e Sandra"
        ></v-text-field>
           <br>
        <v-btn @click="emplenar()">Emplenar</v-btn>
        
        <v-btn @click="enviar">Enviar</v-btn>
            
        <br>
        <v-text-field
            label="Escrui el teu nom"
            solo
            ></v-text-field>
            <v-text-field
            label="Escrui el teu nom"
            outlined
            shaped
            ></v-text-field>
            <v-text-field
            label="Escrui el teu nom"
            filled
            shaped
            ></v-text-field>
            <v-text-field
            label="Escrui el teu nom"
            outlined
            ></v-text-field>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                nom:""

            }
        },
        methods:{
            enviar(){
                console.log("enviant..")
                console.log(this.nom)
            },
            emplenar(){
                this.nom="Sandra"
            }
        }
    }
</script>