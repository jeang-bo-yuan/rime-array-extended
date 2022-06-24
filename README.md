# 行列30

基於`rime-array30`的修改版本。

## What's new

1. 增加萬用字元反查行列碼
2. 反查行列碼以方括弧框住
3. 去除詞彙字典

4. 新增行列反查注音
5. 取消自動造句功能

## 功能說明

以下簡短說明本方案各種實用功能，其他更詳細說明可參考[Wiki](https://github.com/archerindigo/rime-array/wiki)。

### 詞句連書

支援連續輸入多個字之字碼。每字詞之間可以`\`分隔以增加預測準確性。

### 詞彙輸入

預設使用本方案自帶之行列詞庫，符合行列官方詞彙取碼規則（可參考[行列教室](https://www.facebook.com/notes/335303977574152/)最尾部份或[FISH UP行列教學](https://array30.misterfishup.com/tutorial-complete.html#entering-words)）。詞彙以`'`作尾碼。

本方案亦可改用[八股文](https://github.com/rime/rime-essay)自動造詞，惟不支援`'`尾綴，詞彙候選順位可能會因調頻而置於同碼單字之前。啟用方式請參考array30.dict.yaml之附註。

### 符號組

沿用行列官方符號組輸入方式。輸入`w`+`數字`鍵即可選取各符號分組。

### Emoji建議

從方案選單 `🈚️->🈶️`選擇啓用Emoji建議功能。啓用後，當輸入字詞時相關意思的emoji將會出現在候選列上。例如輸入`9-9-1v`時候選字`笑`下方將出現`😄`及其他相關笑臉emoji。

此功能乃基於[Rime Emoji / 繪文字輸入方案](https://github.com/rime/rime-emoji/)。

由於此功能會影響候選字順序，請斟酌使用。另外亦可使用下述針對行列30使用環境而設計的Unicode Emoji輸入方案。

### Unicode Emoji輸入方案

此為在原行列30的基礎上新增的emoji輸入方案。用家可透過美式鍵盤大階`A-L`行選取emoji。第一層分類如下：

- `A`: 🙂 表情符號 Smileys & Emotion
- `S`: 🧑 人物及身體 People & Body
- `D`: 🐕 動物及自然界 Animals & Nature
- `F`: 🍴 食物及飲料 Food & Drink
- `G`: ✈ 旅行及地點 Travel & Places
- `H`: ⚽ 活動 Activities
- `J`: 💡 物件Objects
- `K`: 🔣 圖標符號 Symbols
- `L`: 🏴 旗織 Flags

所有emoji由二至三個鍵碼組成。更詳細的取碼原則請參考[Wiki](https://github.com/archerindigo/rime-array/wiki/RIME%E8%A1%8C%E5%88%9730-Emoji-Unicode%E8%BC%B8%E5%85%A5%E6%96%B9%E6%A1%88%E8%AA%AA%E6%98%8E)。

### "?"萬用字元

輸入"?"作為單個萬用字元，支援查找二至四碼字。

※欲啟用此功能，需要編譯出`array30_query`的字典文件。`array30_query`輸入方案已附在本代碼庫中。

※由於該字典文件相當龐大，所以會需要花費數十分鐘來編譯；在某些性能較差的系統上（如：手機）甚至可能會在編譯時發生系統崩潰。為了減輕編譯所帶來的負擔，本代碼庫已經將預先編譯好的`array30_query`字典文件附在`array30_query-precompiled`資料夾中。

### 從朙月拼音反查行列30

以`` ` ``鍵開始輸入[拼音](https://github.com/rime/rime-luna-pinyin)以反查行列碼。

※欲啟用朙月拼音反查行列碼的功能，需要編譯出`luna_quanpin`的字典文件。`luna_quanpin`輸入方案來自<https://github.com/rime/rime-luna-pinyin>。

### 簡碼及特別碼選字處理

本方案現時會將特別碼顯示於選字欄的首候選字，同官方輸入規則一樣在輸入特別碼後按空白即可選出該字。

一、二級簡碼暫未編排數字鍵位，同碼的簡碼字只會順序於選字欄列出。

## 授權條款

見 [LICENSE](LICENSE)
