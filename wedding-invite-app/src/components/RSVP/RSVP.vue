<!-- eslint-disable prettier/prettier -->
<template>
    <a-row type="flex" justify="space-around" align="middle">
        <a-col :span="18" :xs="{ order: 1 }" :sm="{ order: 1 }" :md="{ order: 1 }" :lg="{ order: 1 }">
            <a-image
                src="https://media-cldnry.s-nbcnews.com/image/upload/newscms/2019_45/2619891/181026_penguin_couple.jpg"
            />
        </a-col>
        <a-col :span="6" :xs="{ order: 2 }" :sm="{ order: 2 }" :md="{ order: 2 }" :lg="{ order: 2 }" align="middle">
            <p>Roker Hotel, Sunderland</p>
            <p>Friday, September 8th 2023</p>
            <a-button type="primary" ghost>Primary</a-button>
        </a-col>
  </a-row>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({});
</script>
