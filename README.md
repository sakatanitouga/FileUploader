# FileUploader　　
# 概要  
サーバ上にファイルをアップロードするプログラム  
# 環境　　
Windows10　いまのところWindowsOSでの動作は確認済み    
Xampp 8.0.1  
  
# 使用方法  
1.以下のリンクへインストーラをダウンロード  
https://www.apachefriends.org/jp/index.html  
  
2.そのままデフォルトのままインストールを行う。  
セットアップ中に再起動が行われるので注意!!  
  
3.Xamppインストール完了後\xampp\apache\conf\httpd.confを開く    
4.<IfModule   mime_module>….</IfModule>　の中に 以下を追記
```
AddType application/x-httpd-php .php .html
```
5.その後
