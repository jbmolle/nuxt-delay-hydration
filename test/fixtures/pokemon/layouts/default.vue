<template>
<div>
  <header >
    <h1 class="text-3xl font-bold p-5 text-center" @click="invert = !invert" :class="invert ? ['text-blue-700', 'bg-yellow-300'] : ['bg-blue-700 text-yellow-500']">
      <nuxt-link to="/">
        Pokédex - {{ $isServer ? 'Not Hydrated' : 'Hydrated'}}
      </nuxt-link>
    </h1>
  </header>
  <main class="bg-blue-500 py-15">
    <div class=" mx-auto container">
      <Nuxt />
    </div>
  </main>
</div>
</template>
<script>
export default {
  data () {
    return {
      invert: false,
    }
  }
}
</script>
