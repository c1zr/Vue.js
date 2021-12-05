<template>
   <ul>
       <dude v-for="(dude, index) in characters" :key="index">
          
       </dude>
   </ul>

<form @submit.prevent="characters.push(newDude)" class="add-new">
    <input v-model="newDude" type="text" />
</form>

<p class="prewiew">
    {{newDude}}
</p>

</template>

<script>

import Dude from "./components/Dude.vue"
    export default {
        components: {
            Dude,
        },
        data() {
            return {
                newDude: '',
                characters: ['Jake the dog', 'Finn the Human', 'Marceline the Vapire'],
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>