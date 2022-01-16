<template>
  <div id="app">
    <ul>
      <li v-for="(personaje, i) in personajes" :key="i">
        <img :src="getSrcByPersonaje(personaje)" alt="avatar" />
        <p>{{ personaje.name }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      personajes: [
        {
          id: 1,
          name: "Rick Sanchez",
        },
        {
          id: 2,
          name: "Morty Smith",
        },
        {
          id: 3,
          name: "Summer Smith",
        },
        {
          id: 4,
          name: "Beth Smith",
        },
        {
          id: 5,
          name: "Jerry Smith",
        },
        {
          id: 6,
          name: "Abadango Cluster Princess",
        },
        {
          id: 7,
          name: "Abradolf Lincler",
        },
      ],
    };
  },
  methods: {
    getSrcByPersonaje(personaje) {
      return `https://rickandmortyapi.com/api/character/avatar/${personaje.id}.jpeg`;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 100%;
  height: 100%;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  background: url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png")
    no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}

ul {
  list-style: none;
}

ul li {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin: 0.5rem 0rem;
}

ul li p {
  color: green;
  font-weight: 700;
  font-size: 1.5rem;
  padding: 0rem 1rem;
}

img {
  width: 8rem;
  height: 8rem;
  border-radius: 50%;
  border: 1px solid green;
}
</style>
