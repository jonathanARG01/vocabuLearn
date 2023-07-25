<script setup lang="ts">

    import { ref, computed } from 'vue';

    defineProps<{
        name:    String,
        age:     Number,
        isAlive: Boolean
    }>();

    const styleColor = 'color: red;';
    const styleHuman = 'color: green; font-size: 20px;';
    const mt3        = 'margin-top: 30px;';

    // Para trabajar con reactividad se debe usar 'ref'
    const isHuman    = ref(true);
    const active     = true;
    const planets    = ['Jupiter', 'Saturno', 'Marte', 'Tierra', 'Urano', 'Mercurio'];

    const arrayFruits = [
        {
            name: 'Manzana',
            price: 1000,
            description: 'Una manzana verde',
            stock: 10
        },
        {
            name: 'Platano',
            price: 1200,
            description: 'Una platano amarillo',
            stock: 0
        },
        {
            name: 'Melon',
            price: 2000,
            description: 'Un melon con vino',
            stock: 20
        },
        {
            name: 'Frutilla',
            price: 500,
            description: 'Una frutilla roja',
            stock: 15
        }
    ]

    const objeto = {
        name: 'Manzana',
        price: 1000,
        description: 'Una manzana verde'
    }





    const evaluate = computed( () => {

        if ( isHuman.value ) {
            return 'isHuman';
        }

        if ( !isHuman.value ) {
            return 'isNotHuman';
        }

    });

    const toggleHuman = () => {
        isHuman.value = !isHuman.value;
    }

</script>



<template>
	
    <div class="person">

        <!-- <li v-bind:style="styleColor"> Name: {{ name }} </li> -->
        <!-- <ul>
            <li :style="styleColor"> Name: {{ name.toUpperCase() }} </li>
            <li> Age: {{ age }} </li>
            <li> Is alive: {{ isAlive }} </li>
            <li>
                <button>Humano o no</button>
            </li>
        </ul> -->

        <!-- <h1> {{ name }} <span v-bind:style="styleHuman"> ({{ isHuman ? 'Si es humano' : 'No es humano' }}) </span></h1> -->

        <!-- Para usar esta sintaxis el 'v-else' debe estar inmediatamente después del 'v-if' -->
        <!-- <p v-if="isHuman">Como eres humano entonces vienes del planeta tierra</p>
        <p v-else>Como NO eres humano entonces ¿De que planeta vienes?</p> -->

        <!-- A diferencia del 'v-if' que destruye el elemento del html, el 'v-show' le aplica solamente un 'display: none;' -->
        <!-- <p v-show="!active">Esta activo para viajar a Jupiter</p> -->

        <!-- <li v-for="planet in planets"> -->
        <!-- Is really important to link the 'key' atributte to each element -->
        <!-- <ul :style="mt3">
            <li v-for="( planet, index ) in planets" :key="index">
                {{ index + 1 }} - {{ planet }}
            </li>
        </ul> -->

        <!-- Recorrer un arreglo de objetos -->
        <!-- <ul :style="mt3">
            <li v-for="fruit in arrayFruits" :key="fruit.name">
                {{ fruit.name }} - {{ fruit.price }} - {{ fruit.description }}
            </li>
        </ul> -->

        <!-- Recorrer un objeto con su valor y propiedad -->
        <!-- <ul :style="mt3">
            <li v-for="(value, property) in objeto" :key="value">
                {{ property }} : {{ value }}
            </li>
        </ul> -->

        <!-- Recorrer un arreglo de objetos solamente de los que tienen un stock superior a cierta cantidad -->
        <!-- <ul :style="mt3">
            <template v-for="fruit in arrayFruits" :key="fruit.name">
                <li v-if="fruit.stock > 0">
                    {{ fruit.name }} - {{ fruit.stock }}
                </li>
            </template>
        </ul> -->

    </div>

    <div class="person">

        <h1>Hola {{ name.toUpperCase() }}</h1>
        <button v-on:click="toggleHuman">Click on Me</button>
        <p :class="evaluate"> {{ isHuman ? 'Si es humano' : 'No es humano' }} </p>
        <p v-if="isHuman">Vienes del planeta tierra</p>
        <p v-else>No eres humano, ¿de que planeta vienes?</p>
    
    </div>

</template>



<style scoped>

    .person {
        background-color: #000;
        padding: 10px;
    }
    .person ul {
        
    }
    .person ul li {
        font-size: 20px;
        font-weight: 600;
        color: #fff;
    }

    .person h1 {
        font-size: 20px;
        font-weight: 600;
        color: #fff;
        margin-top: 20px;
    }

    .person p {
        font-size: 14px;
        font-weight: 600;
        color: yellow;
        margin-top: 20px;
    }

    .isHuman {
        color: green !important;
    }
    .isNotHuman {
        color: red !important;
    }

</style>
