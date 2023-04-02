<script>
import ProfileImage from './ProfileImage.vue'
import Actions from './Actions.vue'
import Message from './Message.vue'
import Timestamp from './Timestamp.vue'
import User from './User.vue'

export default {
   name: 'tweet',
  components: {
    ProfileImage,
    Actions,
    Message,
    Timestamp,
    User

  }, 
   props: {
    user: Object,
    timestamp: String,
    message: String,
    },
  }; 

</script>


<template>

    <div class="tweet">
      <ProfileImage :image="user.image" />

    <div class="body">
      <div class="top">
        <User :user="user" />
<!--    <span class="user">
          <span class="name">{{ tweet.user.name }}</span>
          <span class="handle">@{{ tweet.user.handle }}</span>
        </span> -->
        <Timestamp :timestamp="timestamp" />
        <!-- <span class="timestamp">{{ tweet.timestamp }}</span> -->
      </div>
      <Message :message="message" />
      <!-- <p class="message">{{ tweet.message }}</p> -->


      <div class="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>




<style scoped>
a {
  color: #42b983;
}
</style>
