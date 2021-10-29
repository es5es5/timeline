<template>
  <main>
    <h1>Events</h1>
    <section>
      <h2>2 December</h2>
      <div class="grid-wrapper">
        <article v-for="index in 8" :key="index">
          <h3>9:00 AM</h3>
          <p>Life finds a way. You know what? It is beets. </p>
          <img src="https://images.fineartamerica.com/images-medium-large-5/maroon-bells-aspen-colorado-black-and-white-photography-by-sai.jpg" alt="Black and white photo of a lake">
        </article>
        <!-- <article>
          <h3>10:00 AM</h3>
          <p>I've crashed into a beet truck </p>
          <img src="https://images.fineartamerica.com/images-medium-large-5/maroon-bells-aspen-colorado-black-and-white-photography-by-sai.jpg" alt="Black and white photo of a lake">
        </article>
        <article>
          <h3>12:30 AM</h3>
          <p>I was part of something special. </p>
          <img src="https://images.fineartamerica.com/images-medium-large-5/maroon-bells-aspen-colorado-black-and-white-photography-by-sai.jpg" alt="Black and white photo of a lake">
        </article>
        <article>
          <h3>13:30 AM</h3>
          <p>Yeah, but your scientists were so preoccupied with whether or not they could, they didn't stop to think if they should. </p>
          <img src="https://images.fineartamerica.com/images-medium-large-5/maroon-bells-aspen-colorado-black-and-white-photography-by-sai.jpg" alt="Black and white photo of a lake">
        </article>
        <article>
          <h3>14:30 AM</h3>
          <p>Just my luck, no ice. God help us, we're in the hands of engineers. </p>
        </article>
        <article>
          <h3>15:30 AM</h3>
          <p>I gave it a cold? I gave it a virus. A computer virus. </p>
        </article>
        <article>
          <h3>16:30 AM</h3>
          <p>God creates dinosaurs. God destroys dinosaurs. God creates Man. Man destroys God. Man creates Dinosaurs. </p>
        </article>
        <article>
          <h3>17:30 AM</h3>
          <p>What do they got in there? King Kong?  </p>
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c8/Eiffel_tower_at_Exposition_Universelle%2C_Paris%2C_1889.jpg/1200px-Eiffel_tower_at_Exposition_Universelle%2C_Paris%2C_1889.jpg" alt="Black and white Mountian view">
        </article> -->
      </div>
    </section>
    <!-- <section>
      <h2>3 Jan</h2>
      <div class="grid-wrapper">
        <article>
          <h3>9:00 AM</h3>
          <p>Life finds a way. You know what? It is beets. </p>
        </article>
        <article>
          <h3>10:00 AM</h3>
          <p>I've crashed into a beet truck </p>
        </article>
        <article>
          <h3>12:30 AM</h3>
          <p>I was part of something special. </p>
        </article>
        <article>
          <h3>13:30 AM</h3>
          <p>Yeah, but your scientists were so preoccupied with whether or not they could, they didn't stop to think if they should. </p>
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c8/Eiffel_tower_at_Exposition_Universelle%2C_Paris%2C_1889.jpg/1200px-Eiffel_tower_at_Exposition_Universelle%2C_Paris%2C_1889.jpg" alt="Black and White Eiffel Tower">
        </article>
        <article>
          <h3>14:30 AM</h3>
          <p>Just my luck, no ice. God help us, we're in the hands of engineers. </p>
        </article>
        <article>
          <h3>15:30 AM</h3>
          <p>I gave it a cold? I gave it a virus. A computer virus. </p>
        </article>
        <article>
          <h3>16:30 AM</h3>
          <p>God creates dinosaurs. God destroys dinosaurs. God creates Man. Man destroys God. Man creates Dinosaurs. </p>
        </article>
        <article>
          <h3>17:30 AM</h3>
          <p>What do they got in there? King Kong?  </p>
          <img src="https://images.fineartamerica.com/images-medium-large-5/maroon-bells-aspen-colorado-black-and-white-photography-by-sai.jpg" alt="Black and white Mountian view">
        </article>
      </div>
    </section> -->
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Home'
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
  @media screen and (max-width: 599px){
    height: 250px;
    object-fit: cover;
  }
}
body{
  background: #2b2a2b;
  color: white;
  margin: 0;
  padding: 0;
}

main{
  padding: 2rem;
  max-width: 1400px;
  margin: auto;

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

.grid-wrapper{

  @media screen and (min-width: 600px){
    display: grid;
    grid-auto-flow: column;
    grid-gap: 1rem;
  }

  @media screen and (min-width: 1025px){
    grid-template-columns: 1fr 2fr 1fr 2fr;
  }
  @media screen and (min-width: 600px) and (max-width: 1024px){
    grid-template-columns: 1fr 2fr;
  }

}

article{
  p{
    font-family: 'Karla', sans-serif;
    font-size: 0.95rem;
    color: #c8c8c8;
  }
  padding-bottom: 1rem;
  border-bottom: $border;

  &:nth-child(4){
    grid-area: 1/2/4/3;
  }

  &:nth-child(8){
    @media screen and (min-width: 1025px){
      grid-area: 1/4/4/-1;
    }
    @media screen and (min-width: 600px) and (max-width: 1024px){
      grid-area: 4/2/8/3;
    }
  }

  &:nth-child(4n+3){
    @media screen and (min-width: 1025px){
      border-bottom: 0;
    }
  }
  &:nth-child(4){
    @media screen and (min-width: 1025px){
      border-right: $border;
      padding-right: 1rem;
    }

  }
  &:nth-child(4n){
    @media screen and (min-width: 600px){
      border-left: $border;
      border-bottom: 0;
      padding-left: 1rem;
    }
  }
}

.footer-note{
  text-align: center;
  font-family: 'Karla', sans-serif;
  font-size: 0.9rem;
  background: white;
  padding: 1rem;
  color: black;
  border-radius: 5px;
  a{
    color: inherit;
    font-weight: 600;
  }
}
</style>
