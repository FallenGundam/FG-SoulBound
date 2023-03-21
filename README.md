# FG-SoulBound
物品的靈魂綁定腳本，當物品綁定後其他玩家將無法使用  
採用uuid綁定非綁定玩家名稱，玩家更換名字可以手動更新綁定  
支持掉落物保護，需使用我的另一個腳本MythicDropProtect掛勾  
綁定後的物品掉落後不會損毀 (killall的話還是會刪除)

![image](https://user-images.githubusercontent.com/54828956/226693463-08518507-1676-4319-82c9-bfef0c7b6b4e.png)

# required:
    spigot or paper 1.13 ~ 1.19
    skript 2.6
    skript-reflect
    ItemNBTAPI
    MythicDropProtect (建議搭配使用)


# config:
  * system: &f[&3&lSoulBound&f]  
  * bind_aliases1: &c靈魂綁定&a   =>  一般綁定，玩家可自行解綁
  * bind_aliases2: &4強制綁定&b   =>  特殊綁定，需管理員才能解綁 (如果你想製作贊助武器限制不能分享 這很管用)  
  * bind_event1: &a使用後自動綁定  =>  綁定標籤，玩家點擊後會自動執行強制綁定
