<template>
<v-container
class="text-center"
>
    <div
     class="text-h2 mt-10"
    >
        Contact
        </div>

        <v-sheet
            class="rounded-xl pa-6 ma-2"
            align="center"
            >
            <div
            class="pa-4"
            >
           <a href="https://lin.ee/eMiWgX2">
           <img 
           src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png" 
           alt="友だち追加" 
           max-width="150px" 
           border="0"
           ></a>

           <div>
               ※こちらはお問合せ専用<br>
               「公式ライン」です。
            </div>
            </div>

            <v-divider></v-divider>

            <div
            class="pa-6"
            >
  <validation-observer
    ref="observer"
    v-slot="{ invalid }"
    name="contact" 
    >

    <validation-provider
    v-slot="{errors}"
    name="お名前"
    rules="required"
    >
          <v-text-field
            v-model="name"
            type="text"
            label="name"
            name="name"
            :error-messages="errors"
          />
    </validation-provider>

    <validation-provider
        v-slot="{errors}"
        name="メールアドレス"
        rules="required|email"
    >
          <v-text-field
            v-model="email"
            type="email"
            label="E-mail"
            name="email"
            :error-messages="errors"
          />
    </validation-provider>

        <validation-provider
            v-slot="{errors}"
            name="メッセージ"
            rules="required"
        >
          <v-textarea
            v-model="message"
            label="message"
            name="message"
            :error-messages="errors"
          />
        </validation-provider>

            <v-text-field
          v-show="false"
          v-model="botfield"
          name="bot-field"
          >
          </v-text-field>

             <form
            name="contact" 
            method="POST" 
            data-netlify="true"
            @click.prevent="submit"
          >

          <input type="hidden" name="form-name" value="contact">
          <input v-model="name" type="hidden" name="name" />
          <input v-model="email" type="hidden" name="email" />
          <input v-model="message" type="hidden" name="message" />

          <div
          class="pa-4"
          >
          <v-btn
            :disabled="invalid"
            type="submit"
            width="100%"
            height="50px"
            class="rounded-pill"
            color="primary"
          >
            送信
          </v-btn>
          </div>
            </form> 
    </validation-observer>

        </div>
        </v-sheet>



</v-container>
</template>

<script>
export default {
    
    data() {
        return {
            contact: "contact",
            name: "",
            email: "",
            message: "",
            botfield: "",
            isSubmit: false,
            isSending: false,
        }
    },
    methods: {
        submit() {
          if (this.isSending) {
            return
          }

            const params = new URLSearchParams()
            params.append('form-name', 'contact')
            params.append('name', this.name)
            params.append('email', this.email)
            params.append('message', this.message)

            if(this.botfield) {
              params.append('bot-field', this.botfield)
            }
            
              this.$axios.$post("/", params)
            .then(() => {
              this.$router.push('/success')
            })
            .catch( err => {
              console.error("error", err)
            })
            .finally(() => {
            })
        }
    }


}
</script>