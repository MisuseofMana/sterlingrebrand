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
      <p class="text-body-1"><span class="text-decoration-underline">Your</span> <strong>independent insurance</strong> solution located in <strong>Greenwood, Indiana</strong>.</p>
    </v-col>
  </v-row>

  <v-card class="pa-10 mb-10" elevation="5">
  <v-row>
      <v-col cols="12" md="7">
          <h2 class="text-h2 mb-5">Just ask for Tom.</h2>
          <p class="text-body-1">At Sterling Insurance, we know that one size doesn't fit all. We meet face-to-face to discuss your unique Medicare plan options. Our goal is to help you find the best plan for your medical, financial, and retirement needs.</p>
    </v-col>
    <v-spacer/>
    <v-col cols="12" sm="8" md="5" class="offset-sm-2 offset-md-0">
      <v-img
        src="/tom-headshot.png?url"
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
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d416.54441826982446!2d-86.11292661201044!3d39.61381789969532!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x886b5d3dc3b0ec9f%3A0x3e739445f84bae9e!2sSterling%20Insurance%20Inc!5e0!3m2!1sen!2sus!4v1723429037607!5m2!1sen!2sus" width="100%" height="450" style="border:0;" allowfullscreen="false" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </v-col>
  </v-row>
  
  <v-row class="mb-10">
    <v-col>
      <v-card class="pa-10" elevation="5">
        <h2 class="text-h2 mb-5">Why Choose Sterling Insurance?</h2>
        <ul class="text-body-1 ml-10 mb-5">
          <li><strong>Personalized Service</strong>: We educate you about what Medicare covers and how to manage potential expenses.</li>
          <li><strong>Wide Range of Carriers</strong>: We represent Anthem, Aetna, United Healthcare, Mutual of Omaha, IU Health, and more, giving you the flexibility to find the right coverage.</li>
        </ul>
        <p class="text-body-1 mb-4">Sterling Insurance is a boutique health insurance agency serving Greenwood, We specialize in assisting seniors with tailored Medicare programs to suit their unique needs. We provide expert guidance to ensure our clients understand their options so they can make informed decisions. Our dedicated team helps seniors prepare for healthcare expenses not covered by Medicare, offering comprehensive solutions for a worry-free future.</p>
        <p class="text-body-1">Trust Sterling Insurance for personalized support and peace of mind when planning your retirement healthcare.</p>
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

  <v-card v-if="!noPostsFound" class="pa-10 mb-10" elevation="5">
  <h2 class="text-h2 mb-8">More From Our Facebook Page</h2>
  <v-row v-for="post in posts" :key="post.id" class="mb-10 mb-md-10">
    <v-col cols="12" md="4">
      <v-img :src="post?.mediaLink"></v-img>
    </v-col>
    <v-col cols="12" md="8">
        <!-- <pre>{{ posts[0] }}</pre> -->
        <div>
          <h3 class="text-h2 mb-3">{{ post?.createdAt }}</h3>
          <p class="text-body-1 mb-2">{{post?.message}}</p>
          <a :href="post?.postUrl" target="_blank" class="text-body-1">See more...</a>
        </div>
      </v-col>
    </v-row>
  </v-card>

      <v-card link="https://www.facebook.com/healthcareinnovatorsindy" class="pa-10 text-center d-flex justify-center" color="info" elevation="5">
       <p class="text-body-1 mr-5">
         Tap here to visit us on Facebook.
       </p>
       <v-icon size="39px">mdi-facebook</v-icon>
      </v-card>
</template>

<script setup>
import { ref, onMounted } from 'vue'
 const posts = ref([])
 const noPostsFound = ref(false)
 onMounted(() => {
  fetchFacebookPosts()
 })
 const formattedDate = (dateString) => {
  const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
  const date = new Date(dateString);
  const month = String(date.getMonth() + 1).padStart(2, '0'); // Months are zero-based
  const day = String(date.getDate()).padStart(2, '0');
  const year = date.getFullYear();
  return `${months[month -1]}, ${day}, ${year}`;
}

const fetchFacebookPosts = async () => {
  try {
    const accessToken = import.meta.env.VITE_FB_AUTH
    const pageId = 'healthcareinnovatorsindy'
    const response = await fetch(`https://graph.facebook.com/${pageId}/posts?fields=message,created_time,attachments{media_type,media,url}&limit=5&access_token=${accessToken}`)
    const data = await response.json()
    console.log(data)
    posts.value = data.data.filter(item => item.message).map(post => {
      return {
        createdAt: formattedDate(post.created_time),
        type: post?.attachments?.data[0]?.media_type,
        mediaLink: post?.attachments?.data[0]?.media?.image?.src,
        postUrl : post?.attachments?.data[0]?.url,
        ...post
      }
    })
  }
  catch (error) {
    noPostsFound.value = true
    console.error(error)
  }
}
</script>
