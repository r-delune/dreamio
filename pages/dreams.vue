<template>
  <div class="container">   
    <div>
        <logo />
        <h1>Dreams</h1>
        <!-- <h2>{{type}}</h2> -->
        <h5>{{intro}}</h5>   
        <div  class="row p-3 text-left" v-for="(item, i) in entries" :key="i">
            <div class='col'>
                <div>        
                  <h5>
                      {{ item.title }}
                  </h5>
                </div>        
                <div class='row mx-2'>
                  <label>
                      {{ item.content }}
                  </label>
                </div>        
                <div class='row px-5'>
                  <label>
                      <i>
                        - {{ item.author }}
                      </i>
                  </label> 
                </div>        
            </div>              
        </div>
        <div class="row">  
            <div class="links p-2">
              <nuxt-link to="/">
                <a
                href="/"
                target="_blank"
                class="button--green"
                >
                Back
                </a>
              </nuxt-link>
            </div>
        </div>
    </div>
</div>
</template>
<script>
import Logo from '~/components/Logo.vue'
import { mapState } from 'vuex';
export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  layout: 'default',  
  transition: {
    name: 'test',
    mode: 'out-in'
  },
  components: {
    Logo
  },
  computed: {
    content () {
       console.log('DREAM CONTENT')
       console.log(this.$store.state.dreams.data)
      return this.$store.state.dreams.data
    },
    type () {
      return this.$store.state.dreams.data.title
    },
    intro () {
      return this.$store.state.dreams.data.intro
    },
    entries () {
       console.log('DREAM CONTENT')
       console.log(this.$store.state.dreams.data.entry)
      return this.$store.state.dreams.data.entry
    },
    ...mapState('auth', ['loggedIn', 'user'])
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

</style>
