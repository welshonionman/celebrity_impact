有名人バトルしようぜ！有名人バトル！！各市町村出身の有名人とその影響力を地図上にプロットしてみた(folium + MediaWiki api)

**みんな偉い有名人持ってていいなア！！じゃあ有名人バトルしようぜ！有名人バトル！！**

# なにこれ
自分の出身地と縁のある有名人を挙げてマウントバトルすることがありませんか？  
そんな時、往々にして「どっちも結構有名人だけど、どっちの方が強いか決着がつかねえ…」ということがあると思います。  
そんな時のために、Wikipediaのページ閲覧数をもとに有名人の影響力を定量的に測り、地図上にプロットすることで白黒はっきりさせることが出来る分析ノートブックを作りました。

# どうやったの
Wikipediaの情報を取得できるAPI（MediaWiki api）を使用して、[各都道府県の出身人物のページ](https://ja.wikipedia.org/wiki/Category:%E6%97%A5%E6%9C%AC%E3%81%AE%E9%83%BD%E9%81%93%E5%BA%9C%E7%9C%8C%E5%87%BA%E8%BA%AB%E5%88%A5%E3%81%AE%E4%BA%BA%E5%90%8D%E4%B8%80%E8%A6%A7)からその市町村出身の人物を取得し、その人物のWikipediaページの閲覧数を取得しました。各都道府県の出身人物のページに出身市町村まで載っている人物のみを取得対象としているので、抜け漏れは結構あります。

そして、各市町村ごとにページの閲覧数が最も多い人物を抽出し、foliumというライブラリを使用して地図上にプロットしています。
今回は2022年中の閲覧数をもとにプロットしています。

# どんな感じになったの

作った地図は[ここでグリグリ動かせます。](https://nbviewer.org/github/welshonionman/celebrity_battle/blob/master/celebrity_impact.ipynb)

# やってみてどうよ
- 本当はコロプレス図でもっといい感じにしたかったけど、全国の市町村のポリゴンデータを読み込ませようとするとサイズがでかすぎてフリーズするので断念
- foliumはお手軽にイケてる地図が作れるのでいいぞ
- 
