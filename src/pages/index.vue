<template>
  <v-row>
    <v-col cols="12" class="text-center">
      <v-img
      src="/sterling-insurance-logo-no-text.png?url"
      height="150"
      >
    </v-img>
    <h1 class="text-h1">Sterling Insurance</h1>
  </v-col>
  </v-row>

  <v-row class="mb-10">
    <v-col cols="12" class="text-center">  
      <p class="text-body-1"><span class="text-decoration-underline">Your</span> <strong>Independent Insurance</strong> located in <strong>Greenwood, Indiana</strong></p>
    </v-col>
  </v-row>

  <v-card class="pa-10 mb-10" elevation="5">
  <v-row>
      <v-col cols="12" md="7">
          <h2 class="text-h2 mb-5">Just Ask for Tom.</h2>
          <p class="text-body-1">At Sterling Insurance, we know that one size doesn't fit all. We meet face-to-face to discuss your unique Medicare plan options. Our goal is to help you find the best plan for your medical, financial, and retirement needs.</p>
    </v-col>
    <v-spacer/>
    <v-col cols="12" sm="8" md="5" class="offset-sm-2 offset-md-0">
      <v-img
        src="/tom-cutout.png?url"
        min-width="100px"
        >
      </v-img>
    </v-col>
    <v-spacer/>
  </v-row>
</v-card>

  <v-row class="mb-10">
    <v-col cols="12" class="text-center">
      <p class="text-h2 mb-10">402 W. Main Street, Greenwood, IN, 46142</p>
      <v-row class="text-center">
        <v-col cols="12" md="6" class="d-flex align-center justify-center">
          <v-icon size="40px" class="mr-2">mdi-phone-classic</v-icon>
          <a class="text-h3" href="tel:3178859105">Offices: 317.885.9105</a>
        </v-col>
        <v-col cols="12" md="6" class="d-flex align-center justify-center">
          <p class="text-h3"><v-icon size="40">mdi-cellphone-basic</v-icon></p>
          <a class="text-h3" href="tel:3174080508">Direct: 317.408.0508</a>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
  
  <v-row class="mb-10">
    <v-col cols="12">
      <v-parallax scale=".8" src="/front.jpeg?url"></v-parallax>
    </v-col>
  </v-row>
  
  <v-row class="mb-10">
    <v-col>
      <v-card class="pa-10" elevation="5">
        <h2 class="text-h2 mb-5">Why Choose Sterling Insurance?</h2>
        <ul class="text-body-1 ml-10">
          <li><strong>Personalized Service</strong>: We educate you about what Medicare covers and how to manage potential expenses.</li>
          <li><strong>Wide Range of Carriers</strong>: We represent Anthem, Aetna, United Healthcare, Mutual of Omaha, IU Health, and more, giving you the flexibility to find the right coverage.</li>
        </ul>
      </v-card>
    </v-col>
  </v-row>

  <v-row class="mb-10">
    <v-col>
      <v-card class="pa-10" elevation="5">
          <h2 class="text-h2 mb-5">Key Questions To Consider</h2>
          <ul class="text-body-1 ml-10">
            <li>What hospital systems do I use?</li>
            <li>What physicians do I need to see?</li>
            <li>What dentist do I need to see?</li>
            <li>What optometrist do I need to see?</li>
            <li>What are my financial needs?</li>
          </ul>
      </v-card>
    </v-col>
  </v-row>

  <v-row>
    <v-col>
      <v-card class="pa-10" elevation="5">
        <h2 class="text-h2 mb-5">Facebook Posts</h2>
        <div class="d-flex mb-5" v-for="n in 3">
          <v-card
          height="200"
          width="33%"
          color="yellow"
          />
          <p class="pa-10">Facebook info here</p>
        </div>
      </v-card>
    </v-col>
  </v-row>
</template>

<script setup>
  //
</script>
