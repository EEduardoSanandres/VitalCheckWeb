<template>
    <header>
        <section class="textos-header">
            <h1>VITAL-CHECK</h1>
            <h2>Está enfocada en las farmacias, Para brindar un sistema web
                de control y ventas</h2>
            <button class="button-inicio" role="button">Empieza ahora</button>
        </section>
        <div class="wave" style="height: 150px; overflow: hidden;"><svg viewBox="0 0 500 150" preserveAspectRatio="none"
                                                                        style="height: 100%; width: 100%;">
            <path d="M0.00,49.98 C150.00,150.00 349.20,-50.00 500.00,49.98 L500.00,150.00 L0.00,150.00 Z"
                  style="stroke: none; fill: #fff;"></path>
        </svg></div>
    </header>
    <main>
        <section class="contenedor sobre-nosotros">
            <h2 class="titulo">Sobre nosotros</h2>
            <div class="contenedor-sobre-nosotros">
                <img src="@/assets/PARANOSO.png" alt="" class="imagen-about-us">
                <div class="contenido-textos">
                    <h3><span>1</span>Un sistema sofisticado para la gestión de ventas</h3>
                    <p>Te brindamos un sistema sofisticado con una variedad de opciones para la gestión
                        de ventas que controlara toda tu farmacia.</p>
                    <h3><span>2</span>Un sistema para la venta de tus productos</h3>
                    <p>Te brindamos un sistema con el cual podrás vender tus productos al cliente
                        el cual generara el ticket de venta y así podrás agilizar tus ventas.</p>
                </div>
            </div>
        </section>
        <section class="portafolio">
            <div class="contenedor">
                <h2 class="titulo">INTERFAZ</h2>
                <div class="galeria-port">
                    <div class="imagen-port">
                        <img src="@/assets/img1.jpg" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/img2.jpg" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/logo_fondo.png" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/img1.jpg" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/2intef.png" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/img5.jpg" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/img6.jpg" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                    <div class="imagen-port">
                        <img src="@/assets/1interfas.png" alt="">
                        <div class="hover-galeria">
                            <img src="@/assets/icono1.png" alt="">
                            <p>Nuestro trabajo</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section class="clientes contenedor">
            <h2 class="titulo">NUESTRO SISTEMA ESTA DIRIGIDO PARA</h2>
            <div class="cards">
                <div class="card">
                    <img src="@/assets/dueñofarma.avif" alt="">
                    <div class="contenido-texto-card">
                        <h4>Dueños de farmacia y boticas </h4>
                        <p>Nuestro sistema va dirigido para toda persona que tenga su farmacia
                            y desee un sistema para el control de su farmacia.</p>
                    </div>
                </div>
                <div class="card">
                    <img src="@/assets/PROVEEDOR.png" alt="">
                    <div class="contenido-texto-card">
                        <h4>Proveedor de medicamentos</h4>
                        <p>Nuestro sistema va dirigido también para proveedores que deseen
                            proveer medicamentos con un sistema que pueda hacer el trabajo por ti.</p>
                    </div>
                </div>
            </div>
        </section>
        <section class="about-services">
            <div class="contenedor">
                <h2 class="titulo">PRECIOS</h2>
                <div class="servicio-cont">
                    <div class="servicio-ind">
                        <img src="@/assets/FREE.png" alt="">
                        <h3>VERSION FREE</h3>
                        <p>Prueba gratuita de 15 días para probar el sistema.</p>
                    </div>
                    <div class="servicio-ind">
                        <img src="@/assets/PLUS.png" alt="">
                        <h3>VERSION PLUS</h3>
                        <p>Contarás con todas las opciones del sistema para tu Farmacia.</p>
                    </div>
                    <div class="servicio-ind">
                        <img src="@/assets/PREMIUM.png" alt="">
                        <h3>VERSION PREMIUM</h3>
                        <p>Con la versión premium va dirigido para controlar de 2 a más farmacias.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>
    <footer>
        <div class="contenedor-footer">
            <div class="content-foo">
                <h4>Correo</h4>
                <p>vitalcheck@startup.com</p>
            </div>
            <div class="content-foo">
                <h4>Términos y Condiciones</h4>
                <p>Políticas y privacidad</p>
            </div>
            <div class="content-foo">
                <h4>Location</h4>
                <p>Lima - Perú</p>
            </div>
        </div>
        <h2 class="titulo-final">&copy; VITALCHECK | 2023</h2>
    </footer>
</template>

<script>
export default{
    name: "landing-page",
    data() {  },
    components: {  }
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'open sans';
}

.contenedor {
    padding: 60px 0;
    width: 90%;
    max-width: 1000px;
    margin: auto;
    overflow: hidden;
}

.titulo {
    color: #0043bd;
    font-size: 40px;
    text-align: center;
    margin-bottom: 60px;
}

/* Header */

header {
    width: 100%;
    height: 600px;
    background: #d5dae7;
    /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, hsl(0, 0%, 92%), hsl(0, 0%, 100%)), url(../img/logo_fondo.png);
    /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, hsl(169, 91%, 92%), hsl(77, 92%, 74%)), url(../img/logo_fondo.png);
    /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    background-size: cover;
    background-attachment: fixed;
    position: relative;
}

.button-inicio {
    background: #5E5DF0;
    border-radius: 999px;
    box-shadow: #5E5DF0 0 10px 20px -10px;
    box-sizing: border-box;
    color: #FFFFFF;
    cursor: pointer;
    font-family: Inter,Helvetica,"Apple Color Emoji","Segoe UI Emoji",NotoColorEmoji,"Noto Color Emoji","Segoe UI Symbol","Android Emoji",EmojiSymbols,-apple-system,system-ui,"Segoe UI",Roboto,"Helvetica Neue","Noto Sans",sans-serif;
    font-size: 26px;
    font-weight: 700;
    line-height: 40px;
    opacity: 1;
    outline: 0 solid transparent;
    padding: 8px 18px;
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    width: fit-content;
    word-break: break-word;
    border: 0;
    margin-top: 20px;
}

nav{
    text-align: right;
    padding: 30px 50px 0 0;
}

nav > a{
    color: #292f36;
    font-weight: 300;
    text-decoration: none;
    margin-right: 20px;
    font-weight: bold;
}

nav > a:hover{
    text-decoration: underline;
}

header .textos-header{
    display: flex;
    height: 430px;
    width: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
}

.textos-header h1{
    font-size: 70px;
    color: #e56987;
}

.textos-header h2{
    font-size: 30px;
    font-weight: 300;
    color: #6eb2a0;
    font-weight: bold;
}

.wave{
    position: absolute;
    bottom: 0;
    width: 100%;
}

/* About us */

main .sobre-nosotros{
    padding: 30px 0 60px 0;
}
.contenedor-sobre-nosotros{
    display: flex;
    justify-content: space-evenly;
}

.imagen-about-us{
    width: 48%;
}

.sobre-nosotros .contenido-textos{
    width: 48%;
}

.contenido-textos h3{
    margin-bottom: 15px;
}

.contenido-textos h3 span{
    background: #4d0686;
    color: #fff;
    border-radius: 50%;
    display: inline-block;
    text-align: center;
    width: 30px;
    height: 30px;
    padding: 2px;
    box-shadow: 0 0 6px 0 rgba(0, 0, 0, .5);
    margin-right: 5px;
}

.contenido-textos p{
    padding: 0px 0px 30px 15px;
    font-weight: 300;
    text-align: justify;
}

/* Galeria */


.portafolio{
    background: #f2f2f2;
}

.galeria-port{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
}

.imagen-port{
    width: 24%;
    margin-bottom: 10px;
    overflow: hidden;
    position: relative;
    cursor: pointer;
    box-shadow: 0 0 6px 0 rgba(0, 0, 0, .5);
}

.imagen-port > img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
}

.hover-galeria{
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    transform: scale(0);
    background: hsla(273,91%,27%, 0.7);
    transition: transform .5s;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.hover-galeria img{
    width: 50px;
}

.hover-galeria p{
    color: #fff;
}

.imagen-port:hover .hover-galeria{
    transform: scale(1);
}

/* Clients */

.cards{
    display: flex;
    justify-content: space-evenly;
}

.cards .card{
    background: #4d0686;
    display: flex;
    width: 46%;
    height: 200px;
    align-items: center;
    justify-content: space-evenly;
    border-radius: 5px;
    box-shadow: 0 0 6px 0 rgba(0, 0, 0, 0.6);
}

.cards .card img{
    width: 100px;
    height: 100px;
    object-fit: cover;
    border: 3px solid #fff;
    border-radius: 50%;
    display: block;
}

.cards .card > .contenido-texto-card{
    width: 60%;
    color: #fff;
}

.cards .card > .contenido-texto-card p{
    font-weight: 300;
    padding-top: 5px;
}

/*  Our team */

.about-services{
    background: #f2f2f2;
    padding-bottom: 30px;
}


.servicio-cont{
    display:flex;
    justify-content: space-between;
    align-items: center;
}

.servicio-ind{
    width: 28%;
    text-align: center;
}

.servicio-ind img{
    width: 90%;
}

.servicio-ind h3{
    margin: 15px 0;
    font-weight: bold;
}

.servicio-ind p{
    font-weight: 300;
    text-align: center;
}

/* footer */

footer{
    background: #414141;
    padding: 60px 0 30px 0;
    margin: auto;
    overflow: hidden;
}

.contenedor-footer{
    display: flex;
    width: 90%;
    justify-content: space-evenly;
    margin: auto;
    padding-bottom: 50px;
    border-bottom: 1px solid #ccc;
}

.content-foo{
    text-align: center;
}

.content-foo h4{
    color: #fff;
    border-bottom: 3px solid #af20d3;
    padding-bottom: 5px;
    margin-bottom: 10px;
}

.content-foo p{
    color: #ccc;
}

.titulo-final{
    text-align: center;
    font-size: 24px;
    margin: 20px 0 0 0;
    color: #9e9797;
}

@media screen and (max-width:900px){
    header{
        background-position: center;
    }

    .contenedor-sobre-nosotros{
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .sobre-nosotros .contenido-textos{
        width: 90%;
    }

    .imagen-about-us{
        width: 90%;
    }

    /* Galeria */

    .imagen-port{
        width: 44%;
    }

    /* Clientes */

    .cards{
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .cards .card{
        width: 90%;
    }

    .cards .card:first-child{
        margin-bottom: 30px;
    }

    /* servicios */

    .servicio-cont{
        justify-content: center;
        flex-direction: column;
    }

    .servicio-ind{
        width: 100%;
        text-align: center;
    }

    .servicio-ind:nth-child(1), .servicio-ind:nth-child(2){
        margin-bottom: 60px;
    }

    .servicio-ind img{
        width: 90%;
    }
}

@media screen and (max-width:500px){
    nav{
        text-align: center;
        padding: 30px 0 0 0;
    }

    nav > a{
        margin-right: 5px;
    }

    .textos-header h1{
        font-size: 35px;
    }

    .textos-header h2{
        font-size: 20px;
    }

    /* ABOUT US */

    .imagen-about-us{
        margin-bottom: 60px;
        width: 99%;
    }

    .sobre-nosotros .contenido-textos{
        width: 95%;
    }

    /* Galeria */

    .imagen-port{
        width: 95%;
    }

    /* Clients */

    .cards .card{
        height: 450px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .cards .card img{
        width: 90px;
        height: 90px;
    }

    /* Footer */

    .contenedor-footer{
        flex-direction: column;
        border: none;
    }

    .content-foo{
        margin-bottom: 20px;
        text-align: center;
    }

    .content-foo h4{
        border: none;
    }

    .content-foo p{
        color: #ccc;
        border-bottom: 1px solid #f2f2f2;
        padding-bottom: 20px;
    }

    .titulo-final{
        font-size: 20px;
    }
}
</style>