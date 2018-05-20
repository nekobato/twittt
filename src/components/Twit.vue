<template>
  <li class="twit">
    <div class="account-image-container">
      <img class="account-image" :src="accountImage" />
    </div>
    <span class="account-name" v-show="accountNameIsVisible">@account_name</span>
    <span class="account-nickname" v-show="nickNameIsVisible">Nickname</span>
    <span class="time" v-show="timeIsVisible">YYYY/MM/DD hh:mm:ss</span>
    <p class="message one-line">１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０１２３４５６８７９０</p>
  </li>
</template>

<script>
export default {
  name: 'Twit',
  computed: {
    accountImage () {
      return '/image/account-image-test.png'
    },
    accountNameIsVisible () {
      return true
    },
    nickNameIsVisible () {
      return false
    },
    timeIsVisible () {
      return false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.twit {
  display: flex;
  margin: 0;
  padding: 4px 0;
  border-bottom: 1px solid #ddd;
  text-align: left;
}
.account-image-container {
  flex-shrink: 0;
  position: relative;
  margin: 0 4px;
  width: 48px;
  height: 24px;
  border-radius: 4px;
  overflow: hidden;
}
.account-image {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  margin: auto;
  width: 100%;
  height: 48px;
}
.account-name {
  flex-shrink: 0;
  margin: 0 4px;
  font-size: 12px;
  line-height: 24px;
}
.message {
  margin: 0;
  font-size: 14px;
  line-height: 24px;

  &.one-line {
    white-space: nowrap;
    overflow: hidden;
  }
}
a {
  color: #42b983;
}
</style>
