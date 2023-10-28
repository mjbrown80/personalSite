<template>
  <div id="app">
    <div id="nav">
      <router-link v-bind:to="{ name: 'WelcomePage' }">Home</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'Paintings' }">Paintings</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'Blog' }">Blog</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'About' }">About</router-link>&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'login' }">Login</router-link>
      <router-link v-bind:to="{ name: 'logout' }" v-if="$store.state.token != ''">Logout</router-link>
    </div>
    <router-view />
  </div>
</template>
