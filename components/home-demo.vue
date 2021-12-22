<template>
<v-container>
    <h2>Demo</h2>
      <v-row>
        <v-col>
                <v-card
                height="auto"
                class="rounded-xl pa-2"
                align='center'
                >
                 <h3>URL</h3>
                <v-card-text>
                    <a href="https://lin.ee/tdmSz8a"><img src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png" alt="友だち追加" width="40%" border="0"></a>
                </v-card-text>
                <v-divider></v-divider>
                <h3>QR</h3>
                <v-img src="https://qr-official.line.me/sid/M/336bwogm.png"
                width="50%"
                >
                </v-img>
                
               
                </v-card>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
export default {
    data() {
        return {

        }
    }
}
</script>