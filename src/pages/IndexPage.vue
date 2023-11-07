<template>
  <q-page style="padding: 0.6vmax">
    <q-card flat square class="bg-transparent">
      <q-img src="~assets/PS - Hoja de vida.png" style="height: 24vmax">
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
    <q-card class="bg-transparent" flat sqare>
      <q-card-section>
        <div class="row q-col-gutter-sm">
          <div class="col-lg-3 col-md-3 col-sm-6 col-xs-6 flex flex-center">
            <span
              class="text-weight-bolder text-warning q-pr-sm"
              style="font-size: 1.3vmax"
              >2+</span
            >
            <span class="text-weight-bold text-white text-subtitle2">
              Años de expeiencia</span
            >
          </div>
          <div class="col-lg-3 col-md-3 col-sm-6 col-xs-6 flex flex-center">
            <span
              class="text-weight-bolder text-warning q-pr-sm"
              style="font-size: 1.3vmax"
              >6+</span
            >
            <span class="text-weight-bold text-white text-subtitle2">
              Proyectos culminados</span
            >
          </div>
          <div class="col-lg-3 col-md-3 col-sm-6 col-xs-6 flex flex-center">
            <span
              class="text-weight-bolder text-warning q-pr-sm"
              style="font-size: 1.3vmax"
              >3+</span
            >
            <span class="text-weight-bold text-white text-subtitle2">
              Proyectos personales</span
            >
          </div>
          <div class="col-lg-3 col-md-3 col-sm-6 col-xs-6 flex flex-center">
            <span
              class="text-weight-bolder text-warning q-pr-sm"
              style="font-size: 1.3vmax"
              >1M +
            </span>
            <span class="text-weight-bold text-white text-subtitle2">
              Ideas por llevar a cabo</span
            >
          </div>
        </div>
      </q-card-section>
      <q-card-section>
        <h5 class="text-weight-bold text-white">Mis Proyectos</h5>
        <div class="row q-col-gutter-sm">
          <div class="col-lg-4 col-md-4 col-sm-6 col-xs-6 q-pa-sm">
            <q-card class="bg-primary" flat sqare>
              <q-card-section>
                <span class="text-weight-bold text-white">Desarrollo Web</span>
              </q-card-section>
              <q-card-section>
                <span class="text-weight-bold text-subtitle2 text-grey-8"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Officiis et dolorum possimus. Labore praesentium, non
                  laudantium accusamus aliquam unde nihil nobis dolorum ad atque
                  quasi facere ratione, debitis, ab reprehenderit!</span
                >
              </q-card-section>
              <q-card-section>
                <q-btn
                  flat
                  color="transparent"
                  text-color="warning"
                  label="Mirarlo ahora >"
                />
              </q-card-section>
            </q-card>
          </div>
          <div class="col-lg-4 col-md-4 col-sm-6 col-xs-6 q-pa-sm">
            <q-card class="bg-primary" flat sqare>
              <q-card-section>
                <span class="text-weight-bold text-white">Diseño</span>
              </q-card-section>
              <q-card-section>
                <span class="text-weight-bold text-subtitle2 text-grey-8"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Officiis et dolorum possimus. Labore praesentium, non
                  laudantium accusamus aliquam unde nihil nobis dolorum ad atque
                  quasi facere ratione, debitis, ab reprehenderit!</span
                >
              </q-card-section>
              <q-card-section>
                <q-btn
                  color="transparent"
                  text-color="warning"
                  flat
                  label="Mirarlo ahora >"
                />
              </q-card-section>
            </q-card>
          </div>
          <div class="col-lg-4 col-md-4 col-sm-6 col-xs-6 q-pa-sm">
            <q-card class="bg-primary" flat sqare>
              <q-card-section>
                <span class="text-weight-bold text-white">Automatización</span>
              </q-card-section>
              <q-card-section>
                <span class="text-weight-bold text-subtitle2 text-grey-8"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Officiis et dolorum possimus. Labore praesentium, non
                  laudantium accusamus aliquam unde nihil nobis dolorum ad atque
                  quasi facere ratione, debitis, ab reprehenderit!</span
                >
              </q-card-section>
              <q-card-section>
                <q-btn
                  flat
                  color="transparent"
                  text-color="warning"
                  label="Mirarlo ahora >"
                />
              </q-card-section>
            </q-card>
          </div>
        </div>
      </q-card-section>
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
