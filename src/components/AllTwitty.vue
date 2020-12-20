<template>
  <div class="user-profile__twoots-wrapper">
    <Twitty
      v-for="twitty in twittys"
      :key="twitty.id"
      :username="twitty.author"
      :twitty="twitty.message"
      :avatar="twitty.image"
    />
  </div>
</template>

<script>
import { twittys } from "../assets/twitty";
import Twitty from "../components/Twitty";

export default {
  name: "AllTwitty",
  components: {
    Twitty,
  },

  data() {
    return {
      twittys,
    };
  },
};
</script>

<style>
</style>
