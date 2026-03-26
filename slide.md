---
marp: true
theme: default
header: "Marpによる高速スライド作成"
style: |
  section {
    font-size: 28px;
    background-repeat: no-repeat /* 共通 */;
  }

  section:not(.cover) {
    background-image: url("slide_template.svg"); /* <- メイン背景のURL */
    background-position: top left; /* <- メイン背景の基準位置 */
    background-size: 1280px; /* <- メイン背景のサイズ */
  }

  section.cover {
    background-image: url("cover_template.svg"); /* ★ 表紙用の背景画像URLを指定 */
    background-position: center center; /* 例: 中央揃え */
    background-size: cover; /* 例: 全体を覆うように調整 */
    /* 表紙ページ特有の他のスタイルがあればここに追加 */
    /* 例: テキストの色を白にするなど */
    /* color: white; */
  }

  h1 {
    font-size: 42px;
  }
  h2 {
    font-size: 36px;
  }
  img {
    max-height: 450px;
    display: block;
    margin: 0 auto;
  }
  a {
    color: #0066cc;
  }

---
<!-- _class: cover -->

# スライドタイトル

## サブタイトル

2026年3月26日

---

## タイトル

### 1. 項目

- テスト

### 2. 項目

- テスト
