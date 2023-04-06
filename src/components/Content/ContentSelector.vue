<script>
export default {
   props: ['activeChat']
}
</script>

<template>
    <div v-if="activeChat == 1">
        asdasdasd  {{ activeChat }}
      </div>
    <div v-else>
        1231231231 {{ activeChat }}
    </div>
</template>