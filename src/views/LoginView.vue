<template>
  <div class="login_content">
    <div class="hero-body">
      <div class="columns is-centered">
        <div class="column is-4 box">
          <h3 class="title has-text-black">Login</h3>
          <hr class="login-hr" />
          <p class="subtitle has-text-black"><b>Please login to proceed.</b></p>
          <div>
            <figure class="avatar">
              <b-image
                :src="require('@/assets/almacen-logo.jpg')"
                alt="Profile photo"
                ratio="1by1"
                rounded
              ></b-image>
            </figure>
            <div>
              <b-field>
                <b-input v-model="email" placeholder="Your Email" />
              </b-field>
              <b-field>
                <b-input v-model="password" placeholder="Your Password" />
              </b-field>
              <b-field>
                <b-checkbox>Remember me</b-checkbox>
              </b-field>
              
              <b-button type="is-primary mb-3" expanded>Login</b-button>
            </div>
          </div>
          <p class="has-text-grey">
            <a href="../">Sign Up</a> &nbsp;·&nbsp;
            <a href="../">Forgot Password</a> &nbsp;·&nbsp;
            <a href="../">Need Help?</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginView',
  data () {
    return {
      email: '',
      password: ''
    }
  }
}
</script>

<style scoped>
.login_content {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  width: 100vw;
  background-image: url('@/assets/almacen.png');
  background-size: cover;
}
.hero.is-success {
  background: #f2f6fa;
}

.avatar {
  width: 150px;
  margin: auto;
  padding-bottom: 30px;
}

.login-hr {
  border-bottom: 1px solid black;
}
.field {
  padding-bottom: 10px;
}
.box {
  padding: 40px;
  text-align: center;
}
</style>
