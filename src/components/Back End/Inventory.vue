<template>
    <div class="card flex flex-wrap gap-2 justify-content-center" style="display: flex;">
       <div class="box1">
        <div class="card flex1">
            <div @mouseenter="visible = true">
                <Sidebar v-model:visible="visible" style="background-color: #D7D7D7; justify-content: left;" >
                    <div class="icon1" >
                        <Button icon="pi pi-box" label="Inventory" @click="visible = true" style="background-color: #E5E5E5; color: black; margin: 4% 0 4% 0" />
                        <Button icon="pi pi-users" label="Providers" @click="visible = true" style="background-color: #E5E5E5;color: black; margin: 4% 0 4% 0"/>
                        <Button icon="pi pi-book" label="Catering" @click="visible = true" style="background-color: #E5E5E5;color: black; margin: 4% 0 4% 0"/>
                        <Button icon="pi pi-chart-bar" label="Reports" @click="visible = true" style="background-color: #E5E5E5;color: black; margin: 4% 0 4% 0"/>
                        <Button icon="pi pi-shopping-cart" label="Sales" @click="visible = true" style="background-color: #E5E5E5;color: black; margin: 4% 0 4% 0"/>
                        <Button icon="pi pi-bell" label="Notifications" @click="visible = true" style="background-color: #E5E5E5;color: black; margin: 4% 0 4% 0"/>
                        <Button icon="pi pi-cog" label="Setting" @click="visible = true" style="background-color: #E5E5E5;color: black; margin: 4% 0 4% 0"/>
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
            <div @mouseenter="añadir=true">
                <Dialog v-model:visible="añadir" modal>
                    <h1>Añadir Imagen</h1>
                    <img :src="medicamento">
                    <div class="">
                        <div class="card" style="margin:none; padding: none; display: flex; flex-direction: row;">
                            <Button icon="pi pi-times" class="boton"  label="Cancelar" @click="cancelar1()"/>
                            <Button icon="pi pi-check" class="boton" label="Confirmar" @click="cancelar1()"/>
                        </div>
                    </div> 
                </Dialog>
            </div>
            <div @mouseenter="agregar=true">
                <Dialog v-model:visible="agregar" modal style="background-color: #D7D7D7; justify-content: center;" >
                    <h1>Agregar Producto</h1>
                    <label>Producto</label><br>
                    <InputText type="text" v-model="value" class="dates"/><br>
                    <label>Cantidad</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <label>Categoría</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <label>Fecha de Caducidad</label><br>
                    <InputText type="date" v-model="value" class="dates" /><br>
                    <label>Proveedor</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <label>Precio de Costo</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <label>Precio de Venta</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <label>Descuento por Volumen de Venta</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <label>Cantidad Volumen de Venta</label><br>
                    <InputText type="text" v-model="value" class="dates" /><br>
                    <div class="card">
                    <Button class="boton" icon="pi pi-download" label="Editar Imagen" @click="añadir=true"/>
                    </div>
                    <div class="">
                        <div class="card" style="margin:none; padding: none; display: flex; flex-direction: row;">
                            <Button icon="pi pi-times" class="boton"  label="Cancelar" @click="cancelar()"/>
                            <Button icon="pi pi-check" class="boton" label="Confirmar" @click="cancelar()"/>
                        </div>
                    </div>   
                </Dialog>
            </div>

            <div @mouseenter="eliminar=true">
                <Dialog v-model:visible="eliminar" modal>
                    <h1>Eliminación de Producto</h1>
                    <p>Para la eliminación de este producto se requiere confimación
                        ¿Deseas eliminar el siguiente producto?
                    </p>
                    <img :src="medicamento">
                    <div class="card1 flex flex-wrap gap-2 justify-content-center">
                        <Button icon="pi pi-times" class="boton"  label="Cancelar" @click="cancelar1()"/>
                        <Button icon="pi pi-user-edit" class="boton"  label="Confirmar" @click="cancelar1()"/>
                    </div>
                </Dialog>
            </div>

            <div @mouseenter="edit=true">
                <Dialog v-model:visible="edit" modal style="width:140%, align-items: left">
                    <h1 style="margin:2%">Producto</h1>
                    <div class="card1 flex flex-wrap gap-2 justify-content-center">
                        <div>
                            <label>Código</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                            <label>Producto</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                            <label>Cantidad</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                            <label>Categoría</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                            <label>Fecha de Ingreso</label><br>
                            <InputText type="date" v-model="value" class="dates"/><br>
                            <label>Fecha de Caducidad</label><br>
                            <InputText type="date" v-model="value" class="dates"/><br>
                            <label>Proveedor</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                            <label>Precio de Costo</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                            <label>Precio de Venta</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                        </div>
                        <img :src="medicamento" style="width: 70%; margin: 2%">
                    </div>
                    <div class="card1 flex flex-wrap gap-2 justify-content-center">
                        <div style="margin:0 0 0 2%">
                            <label>Descuento por Volumen de Venta</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                        </div>
                        <div>
                            <label>Cantidad de Volumen de Venta</label><br>
                            <InputText type="text" v-model="value" class="dates"/><br>
                        </div>
                    </div>
                    <div class="card1 flex flex-wrap gap-2 justify-content-center">
                        <Button icon="pi pi-times" class="boton"  label="Cancelar" @click="cancelar()"/>
                        <Button icon="pi pi-user-edit" class="boton"  label="Editar"  />
                        <Button icon="pi pi-delete-left" class="boton"  label="Eliminar" @click="eliminar=true"/>
                    </div>
                </Dialog>
            </div>
            <div class="box2-2">
                <div class="card" style="padding: none; display: flex; flex-direction: row;">
                    <boton class="boton" @click="agregar=true" label="Agregar Producto"/>
                    <boton class="boton" to="/favoritos" label="Visualizar Favoritos"/>
                    <div v-if="favorito">
                        <Favoritos/>
                    </div>
                    <boton class="boton" @click="filtar=true" label="Filtar Productos"/>
                </div>
            </div>    
            <div class="box2-2">
                <h1>Inventario de Productos</h1>
                <button class="button"  @click="edit=true" style="margin: 0 0 0 2%; padding: 0">
                    <img :src="tabla3">
                </button>

            </div>
       </div>
  
    </div>

</template>

<script>
import tabla3 from "@/assets/tabla3.png";
import medicamento from "@/assets/medicamento.png";
import { ref } from "vue";
import Sidebar from 'primevue/sidebar';
import Dialog from 'primevue/dialog';
import button from "primevue/components/button/Button";
import Button from "primevue/components/button/Button";
import boton from "primevue/components/button/Button";


export default {
    name: 'ReportForm',
    components: {
        Sidebar,
        Dialog,
        Button,
        button,
        boton,

    },
    setup(){
        const visible = ref(false);
        const agregar = ref(false);
        const añadir = ref(false);
        const filtar = ref(false);
        const edit = ref(false);
        const eliminar = ref(false);
        return { visible, agregar, filtar, añadir,edit, eliminar };
    },
    data() {
        return {
            tabla3: tabla3,
            medicamento: medicamento,
        }
    },
    methods: {
        cancelar() {
            this.agregar = false;
            this.filtar = false;
            this.edit=false;

        },
        cancelar1() {
            this.añadir = false;
            this.eliminar = false;
        }
    }
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
    width: 120%;
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
    height: 50%;
    text-align: right;
    background-color: #DADADA;
    display: block;
} 

h1
{
    font-size: 200%;
    text-align: center;
    color:#B7334D;
}
.card1
{
    display: flex;
    align-items: center;
}
</style>