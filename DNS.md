# DNS(Dmain,Name,System)とは  
・IPアドレスをドメイン名に変換する仕組みのこと  
ex) github.com <-人間に読みやすい、覚えやすい名前（ドメイン表記）  
一方インターネット上の住所はIPアドレスでも表される  
->ドメイン名はIPアドレスに紐づけられている  
digコマンドで確認
$> dig github.com
```
;; ANSWER SECTION:
github.com.		59	IN	A	13.114.40.48

;; Query time: 9 msec
;; SERVER: 8.8.8.8#53(8.8.8.8)
;; WHEN: Sun Jun 14 20:12:23 JST 2020
;; MSG SIZE  rcvd: 55
```  
<dl>
<dt>正引き</dt>  
<dd>ドメインからIPを見つける仕組み->command:[$>dig ドメイン + short]</dd>
<dt>逆引き</dt>   
<dd>IPからドメインを見つける仕組み->command:[$>dig -x IPアドレス]</dd>  
<dl>  

## DNSレコード    
・ドメインの詳細データのこと
