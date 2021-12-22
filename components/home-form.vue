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

                <v-divider class="ma-5"></v-divider>
                <validation-observer
                v-slot="{ invalid }"
                >
                <v-form
                
                >
                
                    <h3>e-mail</h3>
                    <validation-provider
                    v-slot="{errors}"
                    name="お名前" 
                    rules="required"
                    >
                    <v-text-field
                    v-model="name"
                    label="お名前"
                    :success="valid"
                    :error-messages='errors'
                    >
                    </v-text-field>
                    <p
                    align='left'
                    class=""
                    >{{ name }}</p>
                    </validation-provider>

                    <validation-provider
                    v-slot="{errors}"
                    name="メールアドレス" 
                    rules="required|email"
                    >
                    <v-text-field
                    v-model="email"
                    label="メールアドレス"
                    :success="valid"
                    :error-messages='errors'
                    >
                    </v-text-field>
                    </validation-provider>

                    <validation-provider
                    v-slot="{errors}"
                    name="お問合せ内容" 
                    rules="required"
                    >
                    <v-textarea
                    v-model="msg"
                    label="お問合せ内容"
                    :success="valid"
                    :error-messages='errors'
                    >
                    </v-textarea>
                    </validation-provider>
                    <v-btn
                    width="100%"
                    height="50px"
                    color="primary"
                    type="submit"
                    class="mt-5"
                    :disabled="invalid"
                    >
                        送信
                    </v-btn>
                </v-form>
                </validation-observer>
            </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
export default {
    
    data() {
        return{
            name: '',
            email: '',
            msg: ''
        }
    },
//     methods: {
//     async submit () {
//       const isValid = await this.$refs.observer.validate();
//       if (!isValid) {
//         // バリデーションが通る前に送信ボタンがクリックされた場合の処理
//         alert('out')
//       }
//        // バリデーションが通っている状態で送信ボタンがクリックされた場合の処理
//     }
//   }

}
</script>