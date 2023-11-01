# 建立GCP專用的 SSH 連線設定

[![hackmd-github-sync-badge](https://hackmd.io/scaDi-aqTxG686PjdbvzJQ/badge)](https://hackmd.io/scaDi-aqTxG686PjdbvzJQ)



```
首先要先去下載【PuTTY】這個程式，下載完成後去搜尋的地方打上PuTTY，接下來後面會跳出下方兩個程式`
那我們這邊選【PuTTYgen】這個程式。
```

![](https://i.imgur.com/MWRI8ZO.png)

```
打開之後，我們東西都先不用設定，如下圖
```
![](https://i.imgur.com/StNndgF.png)
**`之後我們先點【Generate】這個按鈕，按下去之後 不知道是我個人問題還是他就是要這樣點，我會一直點他 那個進度條才會跑得快，否則他是跑很慢的 可以去試試看，這邊只是做教學。`**

```
好了之後他會出現以下圖片的內容
```
![](https://i.imgur.com/gvW6McB.png)
- 中間的Key comment 那邊原本有輸入文字，請更改成你登入GCP主機的那個帳號 如下圖
![](https://i.imgur.com/ribNBZ1.png)

```
其他東西都不用設定，但下方打完帳號之後，須把上面的【Key】全部複製起來，並回到GCP主機介面
```
![](https://i.imgur.com/vzuocyq.png)

```
接下來到GCP主機這邊的安全性與存取權這邊，在下方有個【新增項目】的按鈕，請按下那顆按鈕
```
![](https://i.imgur.com/e8ax0Lw.png)
- 他就會跳出一個新的可以讓你輸入的一個金鑰框框，你就把你剛剛複製的Key貼上在那邊
```
輸入完畢之後，點選保存。
```
---

```
接下來我們開啟PuTTY這個程式。
```
![](https://i.imgur.com/yZYgAtA.png)

> 首先要先輸入【主機IP】
> 接下來點左邊的列表，有一個叫【SSH】
> 再點進去有一個叫【Auth】
> 之後什麼東西都不用改，不用點
> 只要看到裡面有，如下圖
![](https://i.imgur.com/ksXr0tH.png)
> 點右邊的【瀏覽】
> 選取你剛剛在【PuTTYgen】存檔的那個Key碼檔案，副檔名會叫[ 什麼什麼.ppk ] 下圖範例
![](https://i.imgur.com/uXAVPnw.png)
> 選好之後，回到左邊選單，往上滑，點選第一個【Session】回來主頁面
---
```
接下來輸入這裡 【Saved Sessions】 名稱建議都是取英文會比較好，像是我都會取【gcp_XXX】這樣做代表
```
![](https://i.imgur.com/tlumm6N.png)

> 名稱打好之後，按右邊的【Save】做存檔

```
存檔完畢之後，點Open進去，之後就正常顯示，到輸入帳號的地方，需要打上你本來在GCP網頁上所顯示的使用者名稱，如下圖
```
![](https://i.imgur.com/F17zO7F.png) 
> ⬆️這個是GCP網頁進入的使用者帳號

![](https://i.imgur.com/Hxuo7PZ.png)
> ⬆️這個是你在PuTTY登入進入後要打的使用者名稱，這樣才可以進哦

# 重點注意!!!
* 設定的Gmail要跟你的GCP帳號是要一樣的
* 如不知道使用者名稱，請先去GCP主機網頁登入裡面查看
* 金鑰務必要設定成【Private/私人專用】的金鑰，只限制於自己或是別人
* 此方式僅限至於【Linux】系統框架的主機，微軟Windows系統框架不支援

### ***本人第一次打這個教學 如有不完整或是有漏缺的請見諒 下次會再改進***