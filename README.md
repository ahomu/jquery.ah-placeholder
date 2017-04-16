# jQuery ah-placeholder Plugin

*A plugin support placeholder attribute alternative.*

HTML5の仕様にあるplaceholder属性を、未対応のブラウザでも擬似的に使えるようにするjQueryプラグインです。title属性に入れた文字列を、プレースホルダー用のテキストとして扱います。

## 使い方 - Usage

サンプル:

    <head>
    <script src="./js/jquery.ah-placeholder.js" type="text/javascript" charset="utf-8"></script>
    <script type="text/javascript">
    $(function()
    {
        $('.jq-placeholder').ahPlaceholder({
            placeholderColor : 'silver',
            placeholderAttr  : 'title',
            likeApple        : false
        });
    });
    </script>
    </head>
    <body>
    <form action="" method="get">
        <input type="text" name="string" value="" title="プレースホルダーテキスト" class="jq-placeholder" />
        <input type="submit" name="submit" value="送信" />
    </form>
    </body>

### placeholderAttrオプション

placeholderAttrオプションがplaceholderの場合、placeholderに対応しているブラウザではスクリプトによる処理を行いません。

likeAppleオプションよりも優先されるため、placeholder対応ブラウザでlikeAppleオプションを有効にしたい場合は、placeholder属性以外（title属性など）を指定してください。

### likeAppleオプション

likeAppleオプションがtrueの場合、Focus時点でplaceholderが消えるのでなく文字入力を始めた時点で消える挙動に変更されます。

これは、iOSのMobile Safariや、Safari5.1以降のplaceholderの動作を再現したものです。

## 変更履歴 - Change log

1.2
:  placeholderAttrオプションを追加

1.1
:  likeAppleオプションを追加

## クレジット - Credit

Copyright 2011, Ayumu Sato ( http://havelog.ayumusato.com )