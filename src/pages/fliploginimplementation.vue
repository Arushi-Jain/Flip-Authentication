<template>
  <div class="flex flex-center q-pt-xl">
    <flip-login :flipit="flipit" width= "40%">
   <div slot="front">
     <q-card style="width: 80%;height : 50%;">
      <q-card-title>
        Login
      </q-card-title>
      <q-card-separator />
      <q-card-main>
        <q-input v-model="email" type="email" suffix="@gmail.com" float-label="Type Your Email" />
        <q-input v-model="pass" type="password" float-label="Password" />
        <q-btn class="q-mt-lg" color="secondary" @click = "flipit = !flipit">Login</q-btn><br>
        <q-btn class="q-mt-md" color="secondary" @click = "flipit = !flipit">Not a member, Join now !</q-btn>
     </q-card-main>
    </q-card>
   </div>
   <div slot="back">
    <q-card >
      <q-card-title>
        Sign Up
      </q-card-title>
      <q-card-separator />
      <q-card-main>
        <q-input v-model="name" type="text" float-label="First Name" />
        <q-input v-model="email" type="email" suffix="@gmail.com" float-label="Type Google Email" />
        <q-input v-model="pass1" type="password" float-label="Password" />
        <q-input v-model="pass2" type="password" float-label="Confirm Password" />
        <q-btn  class="q-mt-lg" color="secondary" @click = "flipit = !flipit">Sign Up</q-btn>
      </q-card-main>
    </q-card>
  </div>
</flip-login>
  </div>
</template>

<style>
</style>

<script>
import FlipLogin from '../components/Fliplogin'
export default {
  name: 'Auth',
  data () {
    return {
      email: '',
      show: true,
      pass: '',
      flipit: false,
      name: '',
      pass1: '',
      pass2: ''
    }
  },
  components: {
    FlipLogin
  }
}
</script>
