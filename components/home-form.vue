<template>
<v-container>
    <h2>Inquiries</h2>
    <v-row>
        <v-col>
              <v-card
            class="rounded-xl pa-6"
            align="center"
            >
           <a href="https://lin.ee/eMiWgX2"><img src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png" alt="友だち追加" width="40%" border="0"></a>
           <v-card-text>※こちらはお問合せ専用<br>「公式ライン」です。</v-card-text>

                <!-- <v-divider class="ma-5"></v-divider>

                 <validation-observer ref="observer" v-slot="{ invalid }" tag="form" @submit.prevent="submit()">
      <text-field-with-validation v-model="first" rules="required" />

      <text-field-with-validation v-model="second" rules="required" />

    <button :disabled="invalid">Submit</button>
  </validation-observer> -->
            </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
export default {
    
    data() {
        return{

        form: {
            name: '',
            email: '',
            msg: '',
            first: '',
            second: ''
        }
        }
    },
    methods: {
         submit() {
            
        this.$refs.observer.reset()
        }
    }


}
</script>