# FileUploader　　
# 概要  
サーバ上にファイルをアップロードするプログラム  
# 環境　　
Windows10　いまのところWindowsOSでの動作は確認済み    
Xampp 8.0.1  
  
# セットアップ方法  (サーバ側)
1.以下のリンクへインストーラをダウンロード  
https://www.apachefriends.org/jp/index.html  
  
2.そのままデフォルトのままインストールを行う。  
セットアップ中に再起動が行われるので注意!!  
  
3.Xamppインストール完了後\xampp\apache\conf\httpd.confを開く    
4.```<IfModule   mime_module>….</IfModule>```の中に 以下を追記
```
AddType application/x-httpd-php .php .html
```
5.\xampp\htdocs のディレクト内に以下を入力する。  
```
git clone https://github.com/sakatanitouga/FileUploader.git
```
# 使用方法
1.サーバ側のPCでxampp-control.exeを実行しApachのStartを押す  
2.作っているhtmlの文の中に以下を入力  
```
<form method="post" action="http://localhost/FileUploader/" enctype="multipart/form-data">
 <input type="file" name="file" id="up_image" multiple>
 <input type="submit" value="送信">
</form>
```
3.送信ボタンを押すとファイルがサーバ側のFileUploaderのフォルダに保存されます。  
