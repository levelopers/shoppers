<template>
  <div>
    <view v-for="(title, key) in list" :key="key" class="title">{{
      title
    }}</view>
  </div>
</template>
<script lang="ts">
import { Vue,Prop,Component } from "vue-property-decorator";

@Component
export default class List extends Vue {
    @Prop({
     type: Array,
     default: [''], 
     required: true,
     validator: (value) => {
        return true
     }
    })
    list: string[]
}

</script>
