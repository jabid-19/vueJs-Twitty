<template>
  <div class="home">
    <div class="left">
      <CreateTwittyPanel />
    </div>
    <div class="right">
      <AllTwitty />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import AllTwitty from "../components/AllTwitty";
import CreateTwittyPanel from "../components/CreateTwittyPanel";

export default {
  name: "Home",
  components: {
    AllTwitty,
    CreateTwittyPanel,
  },
};
</script>

<style lang="scss" scoped>
.home {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-gap: 50px;
  padding: 50px 5%;
}

.right {
  display: grid;
  grid-gap: 10px;
  margin-bottom: auto;
}
</style>
