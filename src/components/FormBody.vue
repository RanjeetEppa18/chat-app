<template>
  <form @submit.prevent="onSubmit">
    <div class="d-flex flex-item-center align-items-center">
      <hr class="style-two" />
      <div class="form-group">
        <div class="input-group mb-3">
          <div class="input-group-prepend">
            <span class="input-group-text" id="basic-addon1">
              <Icon name="person" fontSize="1.2rem" />
            </span>
          </div>
          <input
            type="text"
            class="form-control"
            placeholder="username"
            v-model="username"
            aria-label="Username"
            aria-describedby="basic-addon1"
          />
        </div>
      </div>
      <div class="form-group">
        <div class="input-group mb-3">
          <input
            type="password"
            class="form-control"
            placeholder="password"
            name="password"
            v-model="password"
          />
          <div class="input-group-append">
            <span class="input-group-text" id="basic-addon1">
              <Icon name="eye" fontSize="1.2rem" />
            </span>
          </div>
        </div>
      </div>
      <AuthButton ref="auth"></AuthButton>
      <hr class="style-two" />
    </div>
  </form>
</template>

<script>
import AuthButton from '@/components/AuthButton.vue'
import Icon from '@/components/Icon.vue'
export default {
  name: 'FormBody',
  data() {
    return {
      username: null,
      password: null
    }
  },
  components: {
    AuthButton,
    Icon
  },
  methods: {
    async onSubmit() {
      if (!this.username || !this.password) return
      this.$refs.auth.loading = true
      try {
        const token = await fetch('http://localhost:5000/signup', {
          method: 'post',
          body: JSON.stringify({
            username: this.username,
            password: this.password
          }),
          headers: {
            'Content-Type': 'application/json'
          }
        })
        this.loading = false
        localStorage.setItem('auth_token', await token.text())

        this.$refs.auth.loading = false
      } catch (error) {
        this.$refs.auth.loading = false
        throw new Error(error)
      }
    }
  }
}
</script>

<style></style>
