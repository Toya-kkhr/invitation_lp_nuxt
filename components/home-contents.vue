<template>
<v-container>
    <h2>Service</h2>
   <v-row 
xs='1'>
        <v-col
        v-for="contents in contents"
            :key="contents"
        cols='12'
        lg='4'
        >
            <v-card
            height="auto"
            class="rounded-xl"
            align='center'
            >
            <img
            :src="contents.img"
            width="200px"
            height="200px"
            class="rounded-circle ma-3"
            style="object-fit:cover;"
            />
            <h3>
            {{contents.title}}  
            </h3>

                <template lang="html">
                    <v-card-text v-html="contents.text">
                    </v-card-text>
                </template>
            </v-card>
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
                text: '<strong>会場のマップ</strong><br><strong>参列のお返事</strong><br><strong>ご祝儀のオンライン決済</strong><br><strong>簡単な質問への自動解答</strong><br>全てLINEで完結！<br><br>送った後は、<br><strong>専用ページで出欠状況確認</strong><br><strong>excelでのダウンロード</strong><br>も可能です。',
                },
                {img: '/reception.jpg',
                title: '席次表/メニュー',
                text: 'ゲストに受付で<br><strong>秘密のコード</strong>を渡しましょう。<br>コードをLINEで送ると<br>メニューと席次表がゲストの手元に届きます。'
                },
                {img: '/entertainment.jpg',
                title: '余興',
                text: '余興の準備には意外と時間がかかります。<br>その手間を無くしより新しい体験へ！<br><strong>クイズ</strong><br><strong>ムービー</strong><br><strong>ドレスの色当て…</strong><br>活用方法は様々！<br>思いを実現に導きます。'
                },
            ],
            }
        }
}
</script>