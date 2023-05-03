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
            <h1>Notificaciones</h1>
            <div class="box2-2">
                <h2>Producto en Riesgo de Agotarse</h2>
                <p>El producto "ibuprofeno" cuenta con 6 unidades y está cerca a agotarse</p>
            </div>
            <div class="box2-2">
                <h2>Producto en Riesgo de Vencimiento</h2>
                <p>El producto "ibuprofeno" está cerca de expirarse</p>
            </div>
            <div class="box2-2">
                <h2>Producto en Riesgo de Agotarse</h2>
                <p>El producto "Paracetamol" cuenta con 20 unidades y está cerca a agotarse</p>
            </div>
            <div class="box2-2">
                <h2>Producto en Riesgo de Agotarse</h2>
                <p>Se venden diariamente 3 unidades de "Vitamina D" y solo se encuentra 9 unidades de este producto en stock</p>
            </div>
        </div>
    </div>

</template>

<script>
import { ref } from "vue";
import Sidebar from 'primevue/sidebar';
import Button from "primevue/components/button/Button";
export default {
    name: "notifications-n",
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
    margin: 0 2% 0 0;
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

.box2{
    background-color: #DADADA;
    flex: 1;
    justify-content: left;
    align-items: left;
    margin: 0 0 0 0;
    text-align: center;
}
h1{
    color: #B7334D;
    font-size: 350%;
}

.box2-2{
    background-color: #319B92;
    margin: 2% 3% 1% 3%;
    border-radius: 20px;
    padding: 0.4% 0 0.4% 1%;
    text-align: left;
}

p
{
    text-align: left;
    padding: 0 0 0 1%
}

</style>