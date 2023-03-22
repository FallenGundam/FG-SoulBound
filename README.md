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

# Command:
> /soulboundAdmin - 權限: sb.admin 管理員指令  
> /soulbound - 玩家指令無權限，開啟綁定介面


# API:
    #> 判斷物品是否為該玩家的物品
    #> SB_Bind_conditions
    #> @param p - player 判定綁定的玩家
    #> @param i - itemstack
    #> @param msg - boolean 是否發送消息
    function SB_Bind_conditions(p:player,i:item,msg:boolean) :: boolean:

    #> 物品是否已綁定
    #> SB_ItemIsBinded
    #> @param i - itemstack
    function SB_ItemIsBinded(i:item) :: boolean:

    #> SB_BindItem
    #> @param p - player
    #> @param i - itemstack
    #> @param type - "normal" or "force" force-強制綁定 
    function SB_BindItem(i:item,p:offlineplayer,type:text) :: item:

    #> SB_unbindItem
    #> @param i - itemstack
    #> @param type - "normal" or "force"
    function SB_unbindItem(i:item,type:text) :: item:


    #> 更新綁定，如果玩家改名可使用此方法更新綁定lore
    #> SB_bindupdate
    #> @param p - player
    #> @param i - itemstack
    function SB_bindupdate(p:player,i:item) :: item:
