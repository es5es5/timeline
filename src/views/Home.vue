<template>
  <main>
    <h1>Timeline</h1>
    <section>
      <h2>2 December</h2>
      <div class="grid-wrapper">
        <article v-for="(item, index) in data" :key="index">
          <h3>9:00 AM</h3>
          <p>{{ item.description }}</p>
          <img :src="require(`@/data/images/${item.file}`)">
        </article>
      </div>
    </section>
    <section>
      <h2>2 December</h2>
      <div class="grid-wrapper">
        <article v-for="index in 8" :key="index">
          <h3>9:00 AM</h3>
          <p>Life finds a way. You know what? It is beets. </p>
          <img src="https://images.fineartamerica.com/images-medium-large-5/maroon-bells-aspen-colorado-black-and-white-photography-by-sai.jpg" alt="Black and white photo of a lake">
        </article>
      </div>
    </section>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { data } from '@/data/index'

export default defineComponent({
  name: 'Home',
  data () {
    return {
      data
    }
  }
})
</script>

<style lang="scss">
*{
  box-sizing: border-box;
}

$border: 1px solid #4d4d4d;
$header-font: 'Poppins', sans-serif;

img{
  width: 100%;
  border-radius: 5px;
}

body{
  background: #2b2a2b;
  color: white;
  margin: 0;
  padding: 0;
}

main{
  padding: 2rem;
  max-width: 600px;
  margin: 0 auto;
}

h1{
  font-family:  $header-font;
}

h2{
  color: #ed666f;
  font-family: $header-font;
  font-weight: 500;
}

h3{
  font-family: $header-font;
  font-weight: 500;
  margin: 0.5rem 0;
}

section {
  margin-bottom: 5rem;
}

article{
  p{
    font-family: 'Karla', sans-serif;
    font-size: 0.95rem;
    color: #c8c8c8;
  }
  padding: 1rem 0;
  border-bottom: $border;

  margin: 0 auto;
}
</style>
