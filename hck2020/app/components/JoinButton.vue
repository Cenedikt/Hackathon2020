<template>
  <div>
    <div>
      Noch 8 von 9
    </div>
    <b-button variant="primary" v-if="isHidden" v-on:onclick="joinButton">Event beitreten</b-button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      evJoinButton: false,
      isHidden: true,
      counter: 8,
      maxAnzahl: 9
    }
  },
  methods: {
    showJoin () {
      if (this.counter >= this.maxAnzahl || this.evJoinButt !== true) {
        this.isHidden = false
      }
    },
    joinButton () {
      if (this.evJoinButton === false) {
        this.evJoinButton = true
        this.counter++
      }
    }
  }
}
</script>
