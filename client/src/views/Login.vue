<template>
    <!-- Login Form -->
    <div class="contain">
      <div class="container-fluid col-sm-5 p-4">
        <div class="row-3 p-5 border border-secondary" style="border-radius: 20px; box-shadow: 0 0 25px grey, 0 0 3px grey">
          <form @submit.prevent="login" class="mx-auto">
            <span style="font-size: 30px">Login</span><br>
            <div class="form-group">
              <label for="email" class="col-form-label">Email</label>
              <div>
                <input type="email" class="form-control" v-model="email">
              </div>
            </div>
            <div class="form-group">
              <label for="password" class="col-form-label">Password</label>
              <div>
                <input type="password" class="form-control" v-model="password">
              </div>
            </div>
            <button type="submit" class="btn btn-primary">Login</button>
            <div style="text-align: center;margin-top: 2em;">
              <p>Or With</p>
              <!-- <div class="g-signin2" data-onsuccess="onSignIn" style="display: flex; justify-content:center"></div><br> -->
            </div>
          </form><br>
        </div>
      </div>
    </div>
  
</template>

<script>
export default {
    name: 'LoginPage',
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        login() {
            let payload = {
                email: this.email,
                password: this.password
            }
            this.$emit('loginSubmit', payload)
        }
    }
}
</script>

<style>

</style>