# sv-gen

## Note
  - **URL、'#'になる部分はデコードしちゃいけない**
    - '#'以降の情報はアンカーとみなされてサーバーに送信されないし
  - ズームが大きくないと道の粒度が下がってしまう問題
    - 小さいので取得して合成するしかない

## API
- [このサイト](https://mapstyle.withgoogle.com/)でスタイルを編集できる
  - 例えばroads-lower.jsonはURLだと以下のようになる(今回はAPI_KEYを使わない方法でやるけど)  
    https://maps.googleapis.com/maps/api/staticmap?key=YOUR_API_KEY&center=47.65,-122.35&zoom=12&format=png&maptype=roadmap&style=feature:administrative%7Cvisibility:off&style=feature:landscape%7Cvisibility:off&style=feature:poi%7Cvisibility:off&style=feature:road%7Ccolor:0x99e9f2%7Cvisibility:simplified%7Cweight:7&style=feature:road%7Celement:labels%7Cvisibility:off&style=feature:transit%7Cvisibility:off&style=feature:water%7Cvisibility:off&size=480x360
- 画像はタイル座標で提供されてる(ZLは1~20)
  - ZL=nならx,yはそれぞれ0から2^n-1まで(原点は北西)

## Sample
- 公式のCoverageを無視して作成した場合
  <details>
    <summary>Cuba</summary>
    <img src="./img/Cuba.png">
  </details>
  <details>
    <summary>North Korea</summary>
    <img src="./img/North-Korea.png">
  </details>
  <details>
    <summary>Algeria</summary>
    <img src="./img/Algeria.png">
  </details>
  <details>
    <summary>China</summary>
    <img src="./img/China.png">
  </details>
