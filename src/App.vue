<template>
  <TheTitle text="Notification Message" />
  <NotificationMessage type="error" header="Oh no!">
    <p>Your flight has been <b>canceled</b>!</p>
  </NotificationMessage>

  <NotificationMessage type="success" header="Oh yeah!">
    <p>Your flight is on time</p>
  </NotificationMessage>

  <NotificationMessage> Good Morning </NotificationMessage>
</template>

<script setup>
import NotificationMessage from "./components/NotificationMessage.vue";
import TheTitle from "./components/TheTitle.vue";
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
