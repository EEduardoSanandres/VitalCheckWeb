<template>
    <div class="card flex flex-wrap gap-2 justify-content-center" style="display: flex;">
       <div class="box1">
        <div class="card flex1">
            <div @mouseenter="visible = true">
                <Sidebar v-model:visible="visible" style="background-color: #D7D7D7; justify-content: left;" >
                    <div class="icon1">
                        <Button icon="pi pi-box" label="Inventory" @click="visible = true" style="background-color: #E5E5E5; color: black;" />
                        <Button icon="pi pi-users" label="Providers" @click="visible = true" style="background-color: #E5E5E5;color: black;"/>
                        <Button icon="pi pi-book" label="Catering" @click="visible = true" style="background-color: #E5E5E5;color: black;"/>
                        <Button icon="pi pi-chart-bar" label="Reports" @click="visible = true" style="background-color: #E5E5E5;color: black;"/>
                        <Button icon="pi pi-shopping-cart" label="Sales" @click="visible = true" style="background-color: #E5E5E5;color: black;"/>
                        <Button icon="pi pi-bell" label="Notifications" @click="visible = true" style="background-color: #E5E5E5;color: black;"/>
                        <Button icon="pi pi-cog" label="Setting" @click="visible = true" style="background-color: #E5E5E5;color: black;"/>
                    </div>
                    <div class="icon1-1" style="align-items: flex-end;">
                        <Button icon="pi pi-sign-out" label="Sign off" style="color: white; " @click="visible = true"/>
                    </div>
                </Sidebar>
            </div>
            <div class="icon1">
                <i class="pi pi-box" @click="visible = true" style="background-color: #E5E5E5;"/>
                <i class="pi pi-users" @click="visible = true" style="background-color: #E5E5E5;"/>
                <i class="pi pi-book" @click="visible = true" style="background-color: #E5E5E5;"/>
                <i class="pi pi-chart-bar" @click="visible = true" style="background-color: #E5E5E5;"/>
                <i class="pi pi-shopping-cart" @click="visible = true" style="background-color: #E5E5E5;"/>
                <i class="pi pi-bell" @click="visible = true" style="background-color: #E5E5E5;"/>
                <i class="pi pi-cog" @click="visible = true" style="background-color: #E5E5E5;"/>
            </div>
            <div class="icon1-1">
                <i class="pi pi-sign-out" @click="visible = true"/>
            </div>
        </div>
       </div>
       <div class="card flex flex-wrap gap-2 justify-content-center">
            <div class="box2-2">
                <div class="card" style="margin:0; padding: 0; display: flex; flex-direction: row;">
                    <boton class="boton" @click="agregar=true" label="Regresar"/>
                </div>
            </div>    
            <div class="box2-2">
                <h1>Inventario de Productos</h1>
                <img :src="tabfav">
            </div>
       </div>
  
    </div>

</template>

<script>
import tabfav from "@/assets/tabfav.png";
import { ref } from "vue";
import Sidebar from 'primevue/sidebar';
import Button from "primevue/components/button/Button";
import boton from "primevue/components/button/Button";

export default {
    name: 'ReportForm',
    components: {
        Sidebar,
        Button,
        boton
    },
    setup(){
        const visible = ref(false);
        const agregar = ref(false);
        const añadir = ref(false);
        const filtar = ref(false);
        return { visible, agregar, filtar, añadir };
    },
    data() {
        return {
            tabfav: tabfav,
        }
    },
};

</script>

<style scoped>
body {
  width: 100%;
}


.flex1{
  height: 100vh;
  flex-direction: column;
}


.box2{
    background-color: #DADADA;
}
.box1{
    background-color: #DADADA;
    flex: 0 0 5%;
    margin: 0 14% 0 0;
}

.box2-2
{
    background-color: #DADADA;
    width: 150%;
    font-size: 160%;
}
.icon1
{
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100%;
    width: 100%;
    padding: 10%;

}
.icon1-1{
    display: flex;
    justify-content: center;
    align-items: flex-end;
    margin-top: auto;
    margin: 0 0 2% 0;
    background-color: #B7334D;
    padding: 2%;
    color: white;
}

i{
    cursor: pointer;
    margin: 10%;
    font-size: 400%;
    text-align: center;
    width: 95%;
    border-radius: 10%;
}

Button{
    background: none;
    border: none;
    cursor: pointer;
    margin: 8%;
    border-radius: 10px;
    width: 95%;
    font-size: 200%;
    text-align: center;
    align-items: center;
    height: 100%;
    padding: 4%;
    color: black;
}

.boton{
    background-color: #B7334D;
    margin: 2%;
    padding: 2%;
    color: white;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    font-size: 100%;
    text-align: center;
    align-items: center;
}
.table
{
    background-color: #DADADA;
}

img{
    width: 100%;
    text-align: center;
    background-color: #DADADA;
} 

h1
{
    font-size: 200%;
    text-align: center;
    margin: 0 0 2% 0;
    color:#B7334D;
}
</style>