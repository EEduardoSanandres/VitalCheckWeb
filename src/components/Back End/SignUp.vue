<template>
    <div class="box-container">
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

       <div>
        <div class="icontainer" style="margin:0">
            <div class="icontainer">
                <div class="icon" style="display: inline-block;">
                    <i class="pi pi-money-bill" style="text-align: left; font-size: 200%;">Inventory Price</i>
                </div>
                <div class="icon" style="display:inline-block">
                    <i class="pi pi-credit-card" style="text-align: left; font-size: 200%;">Ganancia</i>
                </div>
                <div class="icon" style="display:inline-block">
                    <i class="pi pi-users" style="text-align: left; font-size: 200%;">Clientes</i>
                </div>
            </div>
        </div>
        <div class="box2" style="width: 50%;">
            <div class="box">
                <h1>Productos Escasos</h1>
                <img :src="tabla1"> 
            </div>
            <div class="box">
                <h1>Membresía</h1>
                <p>Plan</p>
                <label for="plan">Estandar</label>
                <p>Estado</p>
                <label for="plan">Activo</label>
                <p>Caducidad</p>
                <label for="plan">11/04/2024</label>
            </div>
        </div>
       </div>

       <div class="box3">
            <h1>Últimas Ventas</h1>
            <img :src="tabla2">
       </div>
    </div>
</template>

<script>
import tabla1 from "@/assets/tabla1.png"
import tabla2 from "@/assets/tabla2.png"
import { ref } from "vue";
import Sidebar from 'primevue/sidebar';
import Button from 'primevue/button';

export default {
    name: 'SignUp',
    components: {
        Sidebar,
        Button,
    },
    setup(){
        const visible = ref(false);
        return { visible };
    },
    data() {
        return {
            tabla1: tabla1,
            tabla2: tabla2,
        }
    },
};

</script>

<style scoped>
body {
  width: 100%;
}
.flex{
  display: flex;
  justify-content: center;
  align-items: center;
}

.flex1{
  display: flex;
  justify-content: left;
  align-items: left;
  height: 100vh;
  flex-direction: column;
  
}
.box-container{
  display: flex;
}

.box{
    width: 100%;
    display:inline-table;
    background-color: #DADADA;
    margin: 2% 2% 0 0;
}
.box1{
    background-color: #DADADA;
    flex: 0 0 5%;
    justify-content: left;
    align-items: left;
    margin: 0 1% 0 0;
}

.box2{
    width: 100%;
    display:inline-table;
    background-color: #DADADA;
    margin: 2% 2% 0 0;  
}

.box3{
    background-color: #DADADA;
    justify-content: left;
    align-items: left;
    margin: 6% 1% 0 0;
    padding: none;
    width: 30%;
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
    background-color: #B7334D;
    margin: 0 0 5% 0;
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
    font-size: 100%;
    margin: 5%;
    font-size: 200%;
    border-radius: 10%;
    text-align: center;
}

img
{
    background-color: #DADADA;
}
.table
{
    width: 100%;
    margin: 0;
}

.icontainer{
    white-space: nowrap;
}

.icon{
    display: inline-block;
    margin-right: 10%;
    background-color: #DADADA;
    width: 50%;
}
</style>