<template>
  <v-container>
    <v-layout text-center wrap>
      <v-flex xs12>
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">Material Design Icons</h1>
        <p class="subheading font-weight-regular">
          <a href="https://materialdesignicons.com/" target="_blank">
            Material Design Icons
          </a>
        </p>
        <p>icon名の前に mdi- のプレフィックスをつける必要がある</p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'ContactMail',

  data: () => ({}),
}
</script>
