<template>
  <div class="twoot-item">
    <div class="user-profile__twoot">
      <div class="">
        <img v-bind:src="avatar" alt="" />
      </div>

      <div class="twoot-item__content">
        <div class="twoot-item__user">@{{ username }}</div>
        <div>
          {{ twitty }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Twitty",
  props: {
    username: {
      type: String,
      required: true,
    },
    twitty: {
      type: String,
      required: true,
    },
    avatar: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.twoot-item {
  text-align: left;
  padding: 20px;
  background-color: white;
  border-radius: 5px;
  border: 1px solid #dfe3e8;
  box-sizing: border-box;
  cursor: pointer;
  transition: all 0.25s ease;

  &:hover {
    transform: scale(1.1, 1.1);
  }

  .twoot-item__user {
    font-weight: bold;
    margin-bottom: 10px;
  }
}

.user-profile__twoot {
  display: flex;
  flex-direction: row;

  .twoot-item__content {
    display: flex;
    flex-direction: column;
    padding-left: 10px;
  }
  img {
    width: 50px;
    border-radius: 45%;
  }
}
</style>