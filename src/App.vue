<script setup>
import profilePic from './assets/profile.png'

const user = {
  name: 'Somtochukwu Kevin Ogamba',
  role: 'Computer Science Student',
  bio: 'I am a final year Computer Science student at UNIZIK, passionate about UI/UX Designing and front-end development. Currently learning Vue.js fundamentals.',
  photo: profilePic,
  photoAlt: 'Profile photo of Kevin',
  accentColor: 'rgb(174, 94, 181)',
  available: true,
}
</script>

<template>
  <div class="card">
    <img
      :src="user.photo"
      :alt="user.photoAlt"
      class="profile-pic"
      :style="{ borderColor: user.accentColor }"
    />
    <h1>{{ user.name }}</h1>
    <h2>{{ user.role }}</h2>
    <p class="bio">{{ user.bio }}</p>

    <span class="status" :class="user.available ? 'online' : 'offline'">
      {{ user.available ? 'Available' : 'Unavailable' }}
    </span>
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
  border: 3px solid;
  margin-bottom: 1rem;
}

h1 {
  font-size: 1.3rem;
  margin: 0.5rem 0;
}

h2 {
  font-size: 1rem;
  font-weight: 400;
  color: #aaaaaa;
  margin: 0 0 1rem;
}

.bio {
  font-size: 0.95rem;
  color: #cccccc;
  line-height: 1.5;
}

.status {
  display: inline-block;
  margin-top: 1rem;
  padding: 0.3rem 0.9rem;
  border-radius: 999px;
  font-size: 0.8rem;
}

.online {
  background: rgba(46, 204, 113, 0.2);
  color: #2ecc71;
}

.offline {
  background: rgba(231, 76, 60, 0.2);
  color: #e74c3c;
}
</style>