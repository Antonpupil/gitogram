<template>
  <button class="c-story-user-item" @click="$emit('onPress')">
    <div class="avatar">
      <img :src="avatar" alt="username avatar" class="img" />
    </div>
    <div class="username">{{ username }}</div>
  </button>
</template>

<script>
export default {
  name: 'storyUserItem',
  props: {
    username: {
      required: true,
      type: String
    },
    avatar: {
      required: true,
      type: String
    }
  }
}
</script>

<style lang="scss" src="./storyUserItem.scss" scoped></style>
