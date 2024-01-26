<template>
  <div>
    <ul>
      <li v-for="child in children" :key="child.name">
        Name: {{ child.name }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import {defineComponent, PropType} from "vue";
import Child from "@/types/Child";

  export default defineComponent({
    name: 'Children',
    props: {
      children: {
        required: true,
        type: Array as PropType<Child[]>
      }
    }
  })
</script>