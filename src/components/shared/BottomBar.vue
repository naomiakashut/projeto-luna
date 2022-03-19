<template>
<div class="bottom-bar">
<v-bottom-navigation v-model="value">
    <v-btn value="inicio">
        <router-link to="/home">
            <span>Início</span>
        </router-link>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn value="Filmes">
        <router-link to="/lista">
            <span>Lista de Filmes</span>
        </router-link>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn value="login">
        <router-link to="/">
            <span>Login</span>
        </router-link>

      <v-icon>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>
</div>
</template>

<script>

export default {
  name: 'BottomBar',
  data: () => ({ 
      value: 'recent' 
      }),
};
</script>
<style scoped>
.bottom-bar a{
    text-decoration: none;
}
</style>