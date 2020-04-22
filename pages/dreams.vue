<template>
  <div class="container">   
    <div>
        <h1>Dreams</h1>

        <div class="row">      
            <div v-for="(item, i) in content" :key="i">
                <div class='col'>
                    <!-- <badge type="primary m-2" pill>{{ item }}</badge> -->
                    {{content }}
                    <div class='col mx-2'>
                        <h5>
                            {{ item.title }}
                        </h5>
                        <label>
                            {{ item.content }}
                        </label>
                    </div>    
                    <div class='col mx-2'>
                        <label>
                            {{ item.author }}
                        </label>
                    </div> 
                </div>              
            </div>
        </div>
        <div class="row">      
            <div class="links">
                <a
                href="/"
                target="_blank"
                class="button--green"
                >
                Back
                </a>
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
  components: {
    Logo
  },
  computed: {
    content () {
       console.log('DREAM CONTENT')
       console.log(this.$store.state.dreams.data)
      return this.$store.state.dreams.data
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
