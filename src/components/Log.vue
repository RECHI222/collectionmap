




<template>
  <form>
    <v-text-field
      v-model="name" 
  
      :counter="10"
      label="NickName"
      required

    ></v-text-field>
    <!-- <v-text-field
      v-model="password"
      :error-messages="passwordErrors"
      label="PassWord"
      required
      @input="$v.password.$touch()"
      @blur="$v.password.$touch()"
    ></v-text-field> -->
    
    <router-link to="/Home">linkへ移動</router-link>

    <v-btn
      class="mr-4"
      @click="submit"
    >
      submit
    </v-btn>
    <v-btn @click="clear">
      clear
    </v-btn>
  </form>
</template>

<script lang="ts" setup>
import {ref} from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()

// 例えば、ボタンクリック時にページ遷移させる場合
const submit = () => {
router.push("/Home");
}
const name = ref("")
const clear = ()  =>{}

</script>