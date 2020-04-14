<template>
  <div class="home">
    <home-header></home-header>
  </div>
</template>

<script>
// @ is an alias to /src
import homeHeader from '@/views/home/components/homeHeader'

export default {
  name: 'Home',
  components: {
    homeHeader
  }
}
</script>
