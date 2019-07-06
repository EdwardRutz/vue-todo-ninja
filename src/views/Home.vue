<template>
  <div class="home">
    <h1>Home</h1>
    <v-btn depressed class="pink white--text">Click Me</v-btn>
    <v-btn depressed color="pink">Click Me</v-btn>
    <v-btn flat color="pink">Click Me</v-btn>

    <v-btn depressed class="pink white--text">
      <span>email me</span>
      <v-icon right large>email</v-icon>
    </v-btn>
    <v-btn fab depressed small dark color="purple">
      <v-icon>favorite</v-icon>
    </v-btn>

  </div>
</template>

<script>

  export default {

  }
</script>
