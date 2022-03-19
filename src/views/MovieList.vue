<template>
  <v-data-table
    :headers="headers"
    :items="desserts"
    class="elevation-1"
  >
    <template v-slot:title="{ title }">
      <v-chip
        :color="getColor(title)"
        dark
      >
        {{ title }}
      </v-chip>
    </template>
  </v-data-table>
</template>

<script>
export default {
    name: "MovieList",
  
  created() {
    fetch('../data.js')
      .then(response => response.json())
      .then(json => {
        this.movieList = json;
      })

    }
}
</script>