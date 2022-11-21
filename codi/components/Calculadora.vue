<template>
    <v-container>
        <v-row>
            <v-col cols="6">
                <v-text-field
                    label="Numero 1"
                    v-model="num1"
                    type="number"
                ></v-text-field>

                <v-text-field
                    label="Numero 2"
                    v-model="num2"
                    type="number"
                ></v-text-field>
                <br>
                <v-btn fab @click="sumar">+</v-btn>
                <v-btn fab @click="restar">-</v-btn>
                <v-btn fab @click="multiplicar">*</v-btn>
                <v-btn fab @click="dividir">/</v-btn>
                <v-btn fab @click="netejar">C</v-btn>
            </v-col>
            <v-col cols="6" style="background-image: linear-gradient(to right, #1c87c9, #8ebf42)">
                <h1 style="color:blue">Resultat:</h1>
                <div>{{resultat}}</div>
                <div>La suma es {{laSuma}}</div>
                <div>La resta es {{laResta}}</div>
                <div>La multiplicacio es {{laMultiplicacio}}</div>
                <div>La dividi es {{laDividi}}</div>
            </v-col>
        </v-row>
    </v-container>
    
</template>
<script>
export default {
                

            data(){
                        return {
                            num1:0,
                            num2:0,
                            resultat:0
                        }
            },
            methods:{
                   
                sumar(){
                    var a = parseInt(this.num1)
                    var b =parseInt(this.num2)
                    console.log(typeof(a))
                    this.resultat = a + b
                },
                restar(){
                    var a = parseInt(this.num1)
                    var b =parseInt(this.num2)
                    this.resultat=a-b
                },
                multiplicar(){
                    var a = parseInt(this.num1)
                    var b =parseInt(this.num2)
                    this.resultat=a*b
                },
                dividir(){
                    var a = parseFloat(this.num1)
                    var b =parseFloat(this.num2)
                    this.resultat=a/b
                },
                netejar(){
                    this.num1=0
                    this.num2=0
                    this.resultat=0
                }
            },
            computed:{
                laSuma(){
                    return parseFloat(this.num1)
                    + parseFloat(this.num2)
                },
                laResta(){
                    return parseFloat(this.num1)
                    - parseFloat(this.num2)
                },
                laMultiplicacio(){
                    return parseFloat(this.num1)
                    * parseFloat(this.num2)
                },
                laDividi(){
                    return parseFloat(this.num1)
                    / parseFloat(this.num2)
                }


            }
}
</script>