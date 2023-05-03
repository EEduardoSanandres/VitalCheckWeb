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
    <div class="box2">
        <div class="card box2-2 flex">
            <div class="box ">
                <i class="pi pi-user"></i>
                <h1>Mi Perfil</h1>
            </div>
            <div class="box">
                <i class="pi pi-comments"></i>
                <h1>Soporte</h1>
            </div>
        </div>
        <div class="card box2-2 flex">
            <div class="box">
                <i class="pi pi-id-card"></i>
                <h1>Membresía</h1>
            </div>
            <div class="box">
                <i class="pi pi-cog"></i>
                <h1>Administrador</h1>
            </div>
        </div>
    </div>
    </div>
</template>

<script>

import { ref } from "vue";
import Sidebar from 'primevue/sidebar';
import Button from "primevue/components/button/Button";

export default {
    name: 'settingsForm',
    components: {
    Sidebar,
    Button
},
    setup(){
        const visible = ref(false);
        return { visible };
    }
};

</script>

<style scoped>
body {
  width: 100%;
}
.flex{
  display: flex;
  color: white;
  padding: 5%;
  border-radius: 3%;
  width: 120%;
  text-align: center;
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
.box1{
    background-color: #DADADA;
    flex: 0 0 5%;
    justify-content: left;
    align-items: left;
    margin: 0 25% 0 0;
}

.box2{
    justify-content: center;
}
.box2-2
{
    display: flex;
    align-items: center;
}

.box{
    background-color: #B7334D;    
    box-sizing: border-box;
    color: white;
    font-size: 200%;
    margin: 0 2% 0 2%;
    width: 410px;
    border-radius: 10%;
    text-align: center;
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
    margin: 0 0 2% 0;
    color: white;
}

i{
    cursor: pointer;
    margin: 10% 0 10%;
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

.boton{
    background-color: #B7334D;
    color: white;
    width: 100%;
    height: 100%;
    border-radius: 10%;
    font-size: 100%;
    font-size: 100%;
    border-radius: 10%;
    text-align: center;
}

.table
{
    background-color: #DADADA;
}

@media screen and (max-width: 768px) {
  .box-container {
    flex-direction: column;
  }
  .box1 {
    flex: 1;
  }
  .box2 {
    flex: 2;
  }
  .icon1 {
    padding: 5%;
  }
  i {
    font-size: 200%;
  }
  .icon1-1 {
    margin: 5% 0;
    font-size: 150%;
  }
  Button {
    font-size: 150%;
  }
}
</style>