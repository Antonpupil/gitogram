<template>
  <div class="topline">
    <topline>
      <template #headline>
        <div class="icon">
          <icon name='home' />
        </div>
        <h1>Header</h1>
      </template>
      <template #content>
        <ul class="stories">
          <li class="stories-item" v-for="story in stories" :key="story.id">
            <story-user-item
              :avatar="story.avatar"
              :username="story.username"
              @onPress="handlePress(story.id)"
            />
          </li>
        </ul>
        <h1>Content</h1>
      </template>
    </topline>
  </div>
</template>

<script>
import { topline } from '../../components/topline'
import { icon } from '../../icons'
import { storyUserItem } from '../../components/storyUserItem'
import stories from './data.json'
// import { feedItem } from '../../components/feed'

export default {
  name: 'feeds',
  components: {
    topline,
    icon,
    storyUserItem
    // feedItem
  },
  data () {
    return {
      stories
    }
  }
}
</script>

<style lang="scss" scoped>
.icon {
  color:red;
  width: 50px;
}
</style>

<style lang="scss" src="./feeds.scss" scoped></style>
