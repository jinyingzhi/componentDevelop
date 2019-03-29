<template>
      <div class="listbox">
          <!-- {{options}} -->
          <itemcom v-for="i in options" :key="i.id" :options="i">

          </itemcom>
    </div>
</template>

<script>
import itemcom from "./itemcom.vue"
export default {
    props:["options"],
    components:{itemcom}
}

</script>

<style>

</style>
