<template>
<v-container
class="text-center"
>
    <div
     class="text-h2 ma-10"
    >
        Contact
        </div>

        <v-sheet
            class="rounded-xl pa-6"
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

                        </div>
        </v-sheet>
      <validation-observer
    ref="observer"
    v-slot="{ invalid }"
    >
        <v-form 
        name="contact"
        method="post"
        data-netlify-honeypot="botfield"
        netlify
        @click.prevent="submit"
        >

      <v-text-field
        v-show="false"
        v-model="title"
        name="form-name"
      />

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
            v-model="contents"
            label="message"
            name="message"
            :error-messages="errors"
          />
        </validation-provider>

            <v-text-field
          v-show="false"
          v-model="botfield"
          >
          </v-text-field>

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
    </v-form>
    </validation-observer>


</v-container>
</template>

<script>
export default {
    
    data() {
       return {
            title: "contact",
            name: "",
            email: "",
            message: "",
            botfield: ""
        }
    },
    methods: {
    }


}
</script>