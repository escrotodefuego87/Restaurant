<template>
    <v-container>
        <v-flex class="text-center display-1">
            Efectivo Total
        </v-flex>
        <hr style="border-color:orange; width:210px; margin-left:auto; margin-right:auto; border-bottom-width:3px;"/>
        <br>
        <p class="text-center headline success--text" :color--text=totalGlobalColor()>${{totalGlobal()}}</p>
        <br>
        <v-flex>
            <v-data-table
            :headers="headers"
            :items="datos"
            :sort-by="fecha"
            >
            <template v-slot:item.total="{ item }">
                <p>{{precio(item.cantidad,item.precio)}}</p>
            </template>
            </v-data-table>
        </v-flex>
    </v-container>
</template>
<script>
export default {
    data(){
        return{
            headers:[
                {text:"Concepto",align:"left",value:"concepto"},
                {text:"Fecha",value:"fecha"},
                {text:"Hora",value:"hora"},
                {text:"Cantidad",value:"cantidad"}
            ],
            datos:[
                {concepto:"Compra de frutas",fecha:"",hora:"",cantidad:-1000},
                {concepto:"Venta",fecha:"",hora:"",cantidad:350},
                {concepto:"Venta",fecha:"",hora:"",cantidad:500},
                {concepto:"Pago de salario",fecha:"",hora:"",cantidad:-1000},
            ]

        }
    },
    methods:{
        totalGlobal(){
            window.global=0;
            for(var i=0;i<this.datos.length;i++){
                window.global=(window.global+this.datos[i].cantidad);
            }
            return global;
        },
        totalGlobalColor(){
            if(window.global>=0){
                return success;
            }else{
                return red;
            }
        }
    }
}
</script>