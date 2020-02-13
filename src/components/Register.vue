// eslint-disable-next-line vue/valid-template-root
<template>
<div>
    <h2> Register </h2>
    <input type="email" name="email" placeholder="Enter Email" v-model="email"/><br>
    <input type="password" name="password" placeholder="Enter Password" v-model="password"/><br>
    <button @click="register">Register</button>
</div>
</template>
<script>
import AuthService from '@/services/AuthService'
export default {
  data () {
    return {
      form: {
        email: '',
        password: ''}
    }
  },
  methods: {
    async register () {
      // eslint-disable-next-line no-unused-vars
      const response = await AuthService.register({
        email: this.email,
        password: this.password

      })
    }
  }
}
</script>
