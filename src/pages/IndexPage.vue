<template>
  <q-page style="padding: 0.6vmax">
    <q-card flat square>
      <q-img
        src="~assets/PS - Hoja de vida.png"
        style="width: 98%; height: 24vmax; position: absolute"
      >
        <div class="absolute-bottom-left">
          <q-btn
            color="warning"
            label="contactame"
            href="mailto:juan.lema1408@gmail.com"
          />
        </div>
        <div class="absolute-bottom-right">
          <span class="q-pr-sm">Descargar CV</span>
          <q-btn round size="1vmax" flat @click="downloadCV">
            <q-icon color="white" name="fas fa-file-pdf" />
          </q-btn>
        </div>
      </q-img>
    </q-card>
  </q-page>
</template>

<script setup>
function downloadCV() {
  const filePath = "src/assets/Doc/CV- Juan Andres Lema.pdf";
  const link = document.createElement("a");
  link.href = filePath;
  link.download = "CV - Juan Andres Lema.pdf";
  link.click();
}
</script>
