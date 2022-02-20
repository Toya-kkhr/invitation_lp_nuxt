<template>
<v-container
style="padding:200px 5% ;"
>
    <v-row
    align="center"
    justify="center"
    fill-height
    >
        <v-col
        cols="12"
        sm="6"
        >
            <v-card
            class="text-center pa-3"
            >
                <v-card-title
                class="justify-center"
                >
                    Thank you!!!
                </v-card-title>
                <v-card-subtitle>
                    送信が完了しました。
                </v-card-subtitle>
                <v-card-text>
                    お問合せいただき、ありがとうございます。<br>
                    ご入力いただいたメールアドレスへご返信いたします。
                </v-card-text>
                <v-card-actions
                class="justify-center"
                >
                    <v-btn
                    nuxt
                    to="/"
                    width="80%"
                    height="50px"
                    color="primary"
                    >
                        TOPへ戻る
                    </v-btn>
                </v-card-actions>
            </v-card>
        </v-col>
    </v-row>
    </v-container>
</template>

<script>
export default {
    name: "SuccessPage",
}
</script>