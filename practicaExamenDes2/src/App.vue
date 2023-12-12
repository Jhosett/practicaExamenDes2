<script setup>
import { ref } from 'vue';

let indice = ref(0)

const chats = [
  {
    nombre: 'Carlos',
    mensajes:[
      'Hola',
      'Cómo estás?',
      'Qué tal todo?'
    ]
  },
  {
    nombre: 'Valeria',
    mensajes:[
      'Hola',
      'Cómo estás?',
      'Hiciste la tarea?'
    ]
  },
  {
    nombre: 'Maicol',
    mensajes:[
      'Hola',
      'Cómo estás?',
      'Estás en la U?'
    ]
  }
]

function mostrarMensaje(i) {
  indice.value = i
  //chats.value[i]
}

</script>

<template>
  
<div class="flex">
  <div class="h-[600px] w-[80px] bg-slate-950">
    <div class="mt-3">
      <div class="py-1 mx-auto h-12 w-12">
      <img class="rounded" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT5pjxeZ1dITxV1-a3e8AQPf9B4HXBg4P145g&usqp=CAU" alt="">
      </div>
      <p class="text-gray-500 text-center py-1">Perfil</p>
    </div>
  </div>

  <div class="h-[600px] w-[400px] bg-slate-800">
    <div class="ml-5 mt-4">

      <p class="mb-5 text-gray-300 text-lg">TENDENCIAS</p>

      <div class="mb-12">
        <P class="mb-2 text-gray-400">#titanic</P>
        <P class="mb-2 text-gray-400">#millonarios</P>
        <P class="mb-2 text-gray-400">FinalSemestre:D</P>
        <P class="mb-2 text-gray-400">#UFC</P>
        <P class="mb-2 text-gray-400">#ColombiaMarcha</P>
        <P class="mb-2 text-gray-400">#UFPSO</P>
      </div>

      <p class="text-gray-300 mb-6 text-lg">MENSAJES DIRECTOS</p>

      <div>

        <div class="flex bg-gray-700 mr-5 rounded items-center p-3 mb-2" @click="mostrarMensaje (0)">
          <img class="h-10 w-10 rounded-full ml-3" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLdHZMPuW6L7WYKZU0yds4Hyf8gfXCEGymuA&usqp=CAU" alt="">
          <div class="ml-3 my-auto">
            <p class="text-gray-300 text-base">Marcos Pérez</p>
            <p class="text-gray-400 text-xs mt-[-6px]">Hace 10 minutos</p>
          </div>
        </div>

        <div class="flex bg-gray-700 mr-5 rounded items-center p-3 mb-2" @click="mostrarMensaje (1)">
          <img class="h-10 w-10 rounded-full ml-3" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLdHZMPuW6L7WYKZU0yds4Hyf8gfXCEGymuA&usqp=CAU" alt="">
          <div class="ml-3 my-auto">
            <p class="text-gray-300 text-base">Marcos Pérez</p>
            <p class="text-gray-400 text-xs mt-[-6px]">Hace 10 minutos</p>
          </div>
        </div>

        <div class="flex bg-gray-700 mr-5 rounded items-center p-3 mb-2" @click="mostrarMensaje (2)">
          <img class="h-10 w-10 rounded-full ml-3" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLdHZMPuW6L7WYKZU0yds4Hyf8gfXCEGymuA&usqp=CAU" alt="">
          <div class="ml-3 my-auto">
            <p class="text-gray-300 text-base">Marcos Pérez</p>
            <p class="text-gray-400 text-xs mt-[-6px]">Hace 10 minutos</p>
          </div>
        </div>

      </div>

    </div>
  </div>

  <div class="h-[600px] w-[1000px] bg-slate-700">
    <div class="ml-5">
      <p class="text-gray-300 mb-6 text-lg">{{ chats[indice].nombre }}</p>
      <div class="text-white text-base bg-slate-800 rounded mb-5 mr-5 p-3 border-solid border-gray-400" v-for="(obj,i) in chats[indice].mensajes" :key="i">
        {{ chats[indice].mensajes[i] }}
        <p class="ml-[480px] text-gray-500">25/06/2023 10:55am</p>
      </div>
    </div>
  </div>

  <div class="h-[600px] w-[450px] bg-slate-800">
    <div class="">
      <p class="text-gray-300 text-lg ml-24 mt-5">PUBLICIDAD</p>
      <img class="h-[250px] w-[250px] mx-auto mt-3 rounded-3xl" src="https://static.vecteezy.com/system/resources/previews/002/286/073/non_2x/burger-house-fast-food-meal-advertising-poster-with-rays-and-lettering-inscription-delicious-hamburger-or-cheeseburger-promotional-banner-design-template-illustration-for-restaurant-menu-vector.jpg" alt="">
      <img class="h-[250px] w-[250px] mx-auto mt-3 rounded-3xl" src="https://img.freepik.com/vector-premium/anuncio-detergente-diseno-realista_23-2147915317.jpg" alt="">
    </div>
  </div>

</div>

</template>
