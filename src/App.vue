<template>
  <div>
    Token:
    <button @click="getToken">Get token</button>
  </div>
</template>

<script>
import axios from "axios"

export default {
  data() {
    return {

    }
  },
  methods: {
    async getToken() {
      await axios.post("https://us-central1-icapital-oauth2-firebase.cloudfunctions.net/tokeninfo")
          .then(response => console.log(response)).catch(error => console.error(error))
    }
  }
}
</script>
