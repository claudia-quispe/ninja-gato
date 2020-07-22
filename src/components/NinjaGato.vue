<template>
    <div id="NinjaGato">
        <div class="row">
            <div class="col-sm-6">
                <button type="button" class="btn btn-dark" @click="mostrarPerro">Ayudante de Santa</button>
            </div>
            <div class="col-sm-6">
            <button type="button" class="btn btn-dark" @click="mostrarGato">Bola de Nieve</button>
            </div>
        </div>
        <div class="row">
            <div class="col-sm-12">
                <img :src="imagen" alt class="icon" />
            </div>
        </div>
    </div>
</template>

<script>
const dogImg = require('@/assets/huesos.jpg');
const catImg = require('@/assets/snowball.jpg');

export default {
    name: 'NinjaGato',
    data() {
        return {
           imagen: dogImg
        }
    },
    methods: {
        mostrarPerro() {
            console.log('mostrar perro');
            this.imagen = dogImg;
             
        },
        mostrarGato() {
            console.log('mostrar gato');
            this.imagen = catImg;
        }
    },
    beforeUpdate(){
        alert(`¡Cuidado! La imagen esta a punto de cambiar a ${this.imagen == dogImg ? 'Ayudante de Santa' : 'Bola de Nieve' }`)
    }  
};  
</script>

<style>
.card {
    margin-top: 20px;
    margin-left: 100px;
    margin-right: 50px;
}
.icon {
    margin-top: 40px;
}
</style>


