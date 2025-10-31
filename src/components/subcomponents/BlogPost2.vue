<script>
export default {
  props: {
    id: String,
    subject: String,
    entry: String,
    mood: String
  },
  computed: {
    imgSrc() {
      return `/assets/${this.mood?.toLowerCase() || 'default'}.png`
    }
  }
}
</script>

<template>
  <div class="card my-3" style="width: 22rem;">
    <img class="card-img-top" :src="imgSrc" alt="Mood image" />
    <div class="card-body">
      <h5 class="card-title">{{ subject }}</h5>
      <p class="card-text">{{ entry }}</p>
    </div>
    <div class="card-footer">
      <slot name="delete"></slot>
    </div>
  </div>
</template>
