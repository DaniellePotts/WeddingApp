

<script>export default {
    data() {
        return {
            name: '',
            found: [],
            names: ['Danielle', 'Elliott']
        }
    },
    watch: {
        name: function (value) {
            if (value === '') this.found = []
            else {
                this.found = this.names.filter((n) => n.toLowerCase().includes(value.toLowerCase()))
            }
        }
    }
}</script>
<style>
@media (min-width: 1024px) {
    .venue {
        /* min-height: 100vh;
      display: flex;
      align-items: center; */
    }
}
</style>
<template>
    <div class="venue">
        <input type="text" id="name" v-model="name" />
        <div v-if="found.length > 0">
            <select>
                <option v-for="item in found" value={{item}}>{{ item }}</option>
            </select>
        </div>
    </div>
</template>