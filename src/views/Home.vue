<template>
  <div class="home">
    <h1>{{ $t('message') }}</h1>
    <div>
      <select v-model="$i18n.locale" @change="detectLanguage($event)">
        <option
          v-for="langnguage in languages"
          :key="langnguage"
          :value="langnguage">
          {{ langnguage }}
        </option>
      </select>
    </div>
    <HelloI18n />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloI18n from "@/components/HelloI18n.vue";

export default {
  name: "Home",
  components: {
    HelloI18n,
  },
  data(){
    return {
      languages: ['en', 'fr', 'ar']
    }
  },
  methods: {
    detectLanguage(event){
      event.target.value === 'ar' ? document.body.setAttribute('dir', 'rtl') : document.body.setAttribute('dir', 'ltr');
    }
  }
};
</script>
