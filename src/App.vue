<script setup>
import profilePic from './assets/profile.png'
</script>

<template>
  <div class="card">
    <img :src="profilePic" alt="Profile photo" class="profile-pic" />
    <h1>Somtochukwu Kevin Ogamba</h1>
    <p class="bio">
      I am a final year computer Science student at UNIZIK, passionate about UI/UX Designing
      and front-end development. Currently learning Vue.js fundamentals.
    </p>
  </div>
</template>

<style>
body {

  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: rgb(44, 44, 44);
  font-family: Arial, Helvetica, sans-serif;
}

.card {
  font-family: 'Poppins', Arial, Helvetica, sans-serif;
  background: rgb(45, 45, 45);
  border-radius: 16px;
  padding: 2.5rem;
  text-align: center;
  color: white;
  width: 320px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4);
}

.profile-pic {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid rgb(174, 94, 181);
  margin-bottom: 1rem;
}

h1 {
  font-size: 1.3rem;
  margin: 0.5rem 0;
}

.bio {
  font-size: 0.95rem;
  color: #cccccc;
  line-height: 1.5;
}
</style>