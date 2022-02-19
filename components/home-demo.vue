<template>
<v-container
class="text-center"
>
    <div
     class="text-h2 mt-10"
    >
    Demo
    </div>
      <v-row>
        <v-col>
                <v-sheet
                height="auto"
                class="rounded-xl pa-5 ma-2"
                align='center'
                >

                <div
                class="pa-4"
                >
                    <a href="https://lin.ee/tdmSz8a">
                    <img 
                    src="https://scdn.line-apps.com/n/line_add_friends/btn/ja.png"
                     alt="友だち追加"
                    max-width="150px" 
                    border="0"
                    >
                    </a>
                </div>

                <v-divider></v-divider>

                <div
                class="pa-4 text-subtitle-1 font-weight-bold"
                >
                    QR
                </div>

                <v-img 
                src="https://qr-official.line.me/sid/M/336bwogm.png"
                max-width="200px"
                >
                </v-img>
                
               
                </v-sheet>
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