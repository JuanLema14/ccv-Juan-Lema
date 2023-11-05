<template>
  <q-page style="padding: 0.6vmax;">
    <q-card flat square>
      <q-img
        src="~assets/PS - Hoja de vida.png"
        style="width: 70vmax; height: 24vmax; position: absolute"
      >
        <div class="absolute-bottom-left"><q-btn color="warning" label="contactame" href="mailto:juan.lema1408@gmail.com"/></div>
      </q-img>

    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>
