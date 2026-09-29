<script setup>
import { ref, reactive } from 'vue'
import profilePic from './assets/profile.png'

const user = reactive({
  name: 'Somtochukwu Kevin Ogamba',
  role: 'Computer Science Student',
  bio: 'I am a final year Computer Science student at UNIZIK, passionate about UI/UX Designing and front-end development. Currently learning Vue.js fundamentals.',
  photo: profilePic,
  photoAlt: 'Profile photo of Kevin',
  accentColor: 'rgb(174, 94, 181)',
  available: true,
})

const clickCount = ref(0)

function incrementCount() {
  clickCount.value++
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

    <textarea
      v-model="user.bio"
      class="bio-edit"
      rows="3"
      placeholder="Edit your bio..."
    ></textarea>

    <span class="status" :class="user.available ? 'online' : 'offline'">
      {{ user.available ? 'Available' : 'Unavailable' }}
    </span>

    <div class="counter">
      <button @click="incrementCount">Click Here! {{ clickCount }}</button>
    </div>
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

.bio-edit {
  width: 100%;
  margin-top: 0.75rem;
  padding: 0.6rem;
  border-radius: 8px;
  border: 1px solid #555;
  background: rgb(30, 30, 30);
  color: white;
  font-family: 'Poppins', Arial, sans-serif;
  font-size: 0.85rem;
  resize: none;
  box-sizing: border-box;
}

.counter {
  margin-top: 1rem;
}

.counter button {
  border: none;
  background: rgb(174, 94, 181);
  color: white;
  padding: 0.5rem 1.2rem;
  border-radius: 8px;
  font-size: 0.9rem;
  cursor: pointer;
}

.counter button:hover {
  opacity: 0.85;
}
</style>