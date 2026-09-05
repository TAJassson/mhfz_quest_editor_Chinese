# This repo owner was suzaku

Orginal repo : https://github.com/GrenderG/mhfz_quest_editor/

<img width="1584" height="1033" alt="image" src="https://github.com/user-attachments/assets/39a49b11-96b2-49e7-bf20-c6788132b5c5" />

## EN

mhf_questlists_editor is a c# form that allows you to manage questlist files.  

# Before you use
Below are some important tips for using this repo. Please read them at least once.  
- My reader may not read publicly shared questlist files correctly because it does not have proper structure. Also I don't recommend you to keep using it as it is because the reader doesn't support it for a technical reason. Here's how to fix it.   
Open `list_168.bin` with binary editor(eg.HxD) and check offset 01h. It's a number of quests this file loads. If it is `13`, change it to `0D`, becasue `list_168.bin` has 13 quests in total and it should be described as `0D` in hex but somehow the value is `13` of integers.

- Before you add new quest, deleting these quests is highly recommended from `list_168.bin`.  
![image](https://user-images.githubusercontent.com/89909040/161503024-52d490b4-1a5c-4ead-a501-85fad5a7457d.png)


- You should decrypt quest file itself with a tool called `ReFrontier` before you use `Add` button.
- Each questlist files are able to contain up to 42 quests.
- While you can add new quest to list, you cannot add new list file via editor. Thus, I recommend you not to delete all quests from one of list files. I mean leave at least one quest in list.  
- `Export` button creates new questlist files, and overwrites if there is one there with the same name files.  
- `Save change` button is used to save current selected quest changes.  

# Known issues
- Sometimes `Delete` button doesn't work correctly.

# Build
Don't forget to drop `Stored_Data` folder to the same path where exe created.


## Chinese 

mhf_questlists_editor 是一個 C# 表單程式，可用於管理任務列表（questlist）檔案。

## 使用須知
以下是使用此專案的一些重要提示，請至少閱讀一遍。

本讀取器可能無法正確讀取公開分享的任務列表檔案，因為其結構不正確。基於技術原因，讀取器並不支援這種格式，因此不建議直接使用。修復方法如下：

使用十六進位編輯器（如 HxD）開啟 list_168.bin 並檢查偏移量（offset）01h。這是該檔案載入的任務數量。如果顯示為 13，請將其更改為 0D；因為 list_168.bin 總共有 13 個任務，在十六進位中應表示為 0D，但不知為何其值被寫成了十進位的 13。

在新增新任務之前，強烈建議先從 list_168.bin 中刪除這些任務。

在使用「新增（Add）」按鈕之前，您需要先使用名為 ReFrontier 的工具對任務檔案本身進行解密。

![image](https://user-images.githubusercontent.com/89909040/161503024-52d490b4-1a5c-4ead-a501-85fad5a7457d.png)

每個任務列表檔案最多可包含 42 個任務。

雖然您可以向列表中新增新任務，但無法透過編輯器新增新的列表檔案。因此，建議您不要刪除某個列表檔案中的所有任務，請至少在列表中保留一個任務。

「匯出（Export）」按鈕會建立新的任務列表檔案；如果存在同名檔案，則會直接覆蓋。

「儲存變更（Save change）」按鈕用於儲存目前所選任務的修改。

## 已知問題
有時「刪除（Delete）」按鈕無法正常工作。

## 建置說明
請記得將 Stored_Data 資料夾放到與生成的 exe 檔相同的路徑下。

# Changelog

## v 1.0
- Initial release.

## v1.1
- Added montser icon names, for Diva quest.  
- Fixed Diva quest load issue.

## v1.1.1
- Fixed header type issue.

## v1.1.2
- Added panel and scrollbar to information section.

## v1.2
- Now load entire questlist folder, not each single file.  
- Added new listbox to show loaded file name.  
- Added a label at the bottom of the form that works like a log.  
- Added `Stored_Data` folder to store binary data. Don't delete this.

## v1.3
- Added `Export` button to create and export new questlist files.  
- Added `Add` button to add a new quest to current selected list.  
- Added `Delete` button to delete selected quest from list.  
- Added 2 boxed to show how many quests you've loaded.  
- Changed to form is resizable.

## v1.3.1
- Fixed few small things.

## v1.4
- Added `Save changes` button to save current selected quest changes.  
- Added textbox to show Map name.  
- Added combobox to show monsters and items name and its ID.  

## v1.4.1
- Add name suggestion to both Monster and Item name box.
- Fixed a problem where pressing the `Open` button would clear the listbox regardless of whether you actually selected the questlist folder or not (in case you accidentally pressed the button).
- Fixed a problem with the quest listbox behaving incorrectly after pressing the `Export` button.
- Fixed a problem in which the name and ID in the target field did not match when a quest was selected.

## v1.4.2
- Fixed a problem in which the quest list was not loaded all the way through in the game when the export button was pressed once, then a new quest was added, and the export button was pressed again.
