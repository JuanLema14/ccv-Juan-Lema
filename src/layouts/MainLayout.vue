<template>
  <q-layout view="lHh Lpr lFf" class="bg-dark">
    <div class="row">
      <div class="col-lg-2 col-md-2 col-sm-12 col-xs-12">
        <q-card class="bg-accent" flat square>
          <q-card-section>
            <div class="row flex flex-center">
              <div
                class="col-lg-12 col-md-12 col-sm-12 col-xs-12 flex flex-center"
              >
                <q-avatar style="width: 6vmax; height: 6vmax" color="grey-4">
                  <q-img src="~assets/foto_1.png" style="width: 75%" />
                </q-avatar>
              </div>
            </div>
            <div style="text-align: center" class="flex flex-center q-pt-sm">
              <span class="text-weight-bolder text-white"
                >Juan Andrés Lema</span
              >
              <span class="text-subtitle2 text-grey-8"
                >Desarrollador Full-Stack</span
              >
              <span class="text-subtitle2 text-grey-8">Diseñador UI/UX</span>
            </div>
          </q-card-section>
        </q-card>

        <q-card class="bg-secondary" flat square>
          <q-card-section>
            <div class="row">
              <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                <span class="text-weight-bolder text-white">Pais: </span>
              </div>
              <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 row justify-end">
                <p class="text-grey-8">Colombia</p>
              </div>
            </div>

            <div class="row">
              <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                <span class="text-weight-bolder text-white"
                  >Ciudad - Dep:
                </span>
              </div>
              <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 row justify-end">
                <p class="text-grey-8">Rionegro - Antioquia</p>
              </div>
            </div>

            <!-- <div class="row">
              <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                <span class="text-weight-bolder text-white">Edad: </span>
              </div>
              <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 row justify-end">
                <p class="text-grey-8">23</p>
              </div>
            </div> -->
          </q-card-section>

          <q-separator color="grey-8" />

          <q-card-section>
            <div class="row">
              <div
                class="col-lg-6 col-md-6 col-sm-6 col-xs-12 flex flex-center"
              >
                <q-circular-progress
                  rounded
                  show-value
                  font-size="0.8vmax"
                  :value="engVal"
                  size="5vmax"
                  :thickness="0.2"
                  color="warning"
                  track-color="grey-8"
                  class="q-ma-md"
                >
                  <span class="text-weight-bold text-white">{{ engVal }}%</span>
                </q-circular-progress>
                <span class="text-weight-bold text-white flex flex-center"
                  >Ingles</span
                >
              </div>
              <div
                class="col-lg-6 col-md-6 col-sm-6 col-xs-12 flex flex-center"
              >
                <q-circular-progress
                  rounded
                  show-value
                  font-size="0.8vmax"
                  :value="espVal"
                  size="5vmax"
                  :thickness="0.2"
                  color="warning"
                  track-color="grey-8"
                  class="q-ma-md"
                >
                  <span class="text-weight-bold text-white">{{ espVal }}%</span>
                </q-circular-progress>
                <span class="text-weight-bold text-white flex flex-center"
                  >Español</span
                >
              </div>
            </div>
          </q-card-section>

          <q-separator color="grey-8" />

          <q-card-section>
            <q-carousel
              v-model="habilitiesCarsl"
              transition-prev="scale"
              transition-next="scale"
              ref="carousel"
              control-color="warning"
              class="bg-transparent"
              fit
              swipeable
              animated
              style="height: 14vmax"
            >
              <q-carousel-slide name="1" class="q-pt-xl">
                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">HTML:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      htmlValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="htmlVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">CSS:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      cssValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="cssVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">JS:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      jsValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="jsVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">PHP:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      phpValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="phpVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder"
                      >WordPress:</span
                    >
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      wordPValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="wordPVal" color="warning" />
              </q-carousel-slide>

              <!--Carousel pt2 °°° -->

              <q-carousel-slide name="2" class="q-pt-xl">
                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">SQL:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      sqlValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="sqlVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">Node js:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      nodeValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="nodeVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">Python:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      pythonValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="pythonVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder">Java:</span>
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      javaValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="javaVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder"
                      >Illustrator:</span
                    >
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      illustValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="illustVal" color="warning" />
              </q-carousel-slide>

              <!--Carousel pt3 °°° -->

              <q-carousel-slide name="3" class="q-pt-xl">
                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder"
                      >Servicios AWS:</span
                    >
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      awsValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="awsVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder"
                      >Automatización en Powershell:</span
                    >
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      pshellValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress rounded :value="pshellVal" color="warning" />

                <div class="row q-pa-sm">
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6">
                    <span class="text-white text-weight-bolder"
                      >Administración de servidores web:</span
                    >
                  </div>
                  <div class="col-lg-6 col-md-6 col-sm-6 col-xs-6 justify-end">
                    <span class="row justify-end text-white">{{
                      servWebValLabel
                    }}</span>
                  </div>
                </div>

                <q-linear-progress
                  rounded
                  :value="servWebVal"
                  color="warning"
                />
              </q-carousel-slide>

              <!-- Controles °°° -->

              <template v-slot:control>
                <q-carousel-control
                  position="top-left"
                  :offset="[0, 2]"
                  class="text-white rounded-borders q-pa-md"
                  style="padding: 4px 8px"
                >
                  <q-btn
                    v-if="habilitiesCarsl !== '1'"
                    flat
                    dense
                    text-color="warning"
                    icon="arrow_left"
                    @click="$refs.carousel.previous()"
                  />

                  <q-btn
                    v-if="habilitiesCarsl !== '3'"
                    flat
                    dense
                    text-color="warning"
                    icon="arrow_right"
                    @click="$refs.carousel.next()"
                  />
                </q-carousel-control>
              </template>
            </q-carousel>
          </q-card-section>

          <q-separator color="grey-8" />

          <q-card-section>
            <div class="row">
              <div
                class="col-lg-12 col-md-12 col-sm-12 col-xs-12 row justify-start"
              >
                <q-icon name="check" color="warning" class="q-pa-xs" />
                <p class="text-grey-8">Lorem Ipsum dolor asit amet</p>
              </div>

              <div
                class="col-lg-12 col-md-12 col-sm-12 col-xs-12 row justify-start"
              >
                <q-icon name="check" color="warning" class="q-pa-xs" />
                <p class="text-grey-8">Lorem Ipsum dolor asit amet</p>
              </div>

              <div
                class="col-lg-12 col-md-12 col-sm-12 col-xs-12 row justify-start"
              >
                <q-icon name="check" color="warning" class="q-pa-xs" />
                <p class="text-grey-8">Lorem Ipsum dolor asit amet</p>
              </div>
            </div>
          </q-card-section>

          <q-separator color="grey-8" />
        </q-card>
        <q-card class="bg-accent" flat square>
          <q-car-section>
            <div class="row q-pa-md">
              <div class="col flex flex-center" style="cursor: pointer">
                <q-btn
                  round
                  size="0.7vmax"
                  flat
                  href="https://github.com/JuanLema14/"
                >
                  <q-icon color="white" name="fab fa-github" />
                </q-btn>
              </div>
              <div class="col flex flex-center" style="cursor: pointer">
                <q-btn
                  round
                  size="0.7vmax"
                  flat
                  href="https://www.instagram.com/juanlemat/"
                >
                  <q-icon color="white" name="fab fa-instagram" />
                </q-btn>
              </div>
              <div class="col flex flex-center" style="cursor: pointer">
                <q-btn round size="0.7vmax" flat href="https://w.app/XomzdE">
                  <q-icon color="white" name="fab fa-whatsapp" />
                </q-btn>
              </div>
            </div>
          </q-car-section>
        </q-card>
      </div>
      <div class="col-lg-10 col-md-10 col-sm-12 col-xs-12">
        <q-page-container>
          <router-view />
        </q-page-container>
      </div>
    </div>
  </q-layout>
</template>

<script setup>
import { ref, computed } from "vue";

const habilitiesCarsl = ref("1");

const leftDrawerOpen = ref(true);

const engVal = ref(70);
const espVal = ref(100);

const htmlVal = ref(0.9);
const cssVal = ref(0.7);
const jsVal = ref(0.9);
const phpVal = ref(0.4);
const wordPVal = ref(0.8);
const sqlVal = ref(0.5);
const nodeVal = ref(0.9);
const pythonVal = ref(0.6);
const javaVal = ref(0.8);
const illustVal = ref(0.9);
const awsVal = ref(0.8);
const pshellVal = ref(0.7);
const servWebVal = ref(0.7);

const htmlValLabel = computed(() => (htmlVal.value * 100).toFixed(0) + "%");
const cssValLabel = computed(() => (cssVal.value * 100).toFixed(0) + "%");
const jsValLabel = computed(() => (jsVal.value * 100).toFixed(0) + "%");
const phpValLabel = computed(() => (phpVal.value * 100).toFixed(0) + "%");
const wordPValLabel = computed(() => (wordPVal.value * 100).toFixed(0) + "%");
const sqlValLabel = computed(() => (sqlVal.value * 100).toFixed(0) + "%");
const nodeValLabel = computed(() => (nodeVal.value * 100).toFixed(0) + "%");
const pythonValLabel = computed(() => (pythonVal.value * 100).toFixed(0) + "%");
const javaValLabel = computed(() => (javaVal.value * 100).toFixed(0) + "%");
const illustValLabel = computed(() => (illustVal.value * 100).toFixed(0) + "%");
const awsValLabel = computed(() => (awsVal.value * 100).toFixed(0) + "%");
const pshellValLabel = computed(() => (pshellVal.value * 100).toFixed(0) + "%");
const servWebValLabel = computed(
  () => (servWebVal.value * 100).toFixed(0) + "%"
);
</script>

<style lang="scss" scoped></style>
