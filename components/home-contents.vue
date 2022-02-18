/* eslint-disable vue/no-v-html */
<template>
<v-container
class="text-center"
>

    <div
    class="text-h2 ma-10"
    >
        Service
        </div>

   <v-row>
        <v-col
        v-for="content in contents"
        :key="content"
        cols='12'
        lg='4'
        >
        <v-sheet
        class="rounded-xl pa-4 py-10"
        align='center'
        >
                <v-img
                :src="content.img"
                style="border-radius:50%;"
                width="200px"
                height="200px"
                />
                <div
                class="pa-4 text-subtitle-1 font-weight-bold"
                >
                {{content.title}}  
                </div>

                <div
                class="px-3"
                >
                {{content.text}}
                </div>
            </v-sheet>
        </v-col>
</v-row>
</v-container>
</template>

<script>
export default {
    data() {
        return{
            contents: [
                {img: '/invitation.jpg',
                title: '招待状',
                text: '会場のマップ参列のお返事ご祝儀のオンライン決済簡単な質問への自動解答全てLINEで完結！送った後は、専用ページで出欠状況確認excelでのダウンロードも可能です。',
                },
                {img: '/reception.jpg',
                title: '席次表/メニュー',
                text: 'ゲストに受付で秘密のコードを渡しましょう。コードをLINEで送るとメニューと席次表がゲストの手元に届きます。'
                },
                {img: '/entertainment.jpg',
                title: '余興',
                text: '余興の準備には意外と時間がかかります。その手間を無くしより新しい体験へ！クイズムービードレスの色当て…活用方法は様々！思いを実現に導きます。'
                },
            ],
            }
        }
}
</script>
