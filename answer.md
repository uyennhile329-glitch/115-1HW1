# 第1次作業題目-作業-HW1
>
>學號：112105142
><br />
>姓名：黎鴛兒
><br />
>作業撰寫時間：180 mins（包含程式撰寫時間）
><br />
>最後撰寫文件日期：2026/11/23
>....

本份文件包含以下主題：
- [x] 說明內容
- [x] 其他 (可以包含心得或是想跟老師反映)

## 說明內容

1. 請參閱 Topic 0 的 git clone 該頁 (P. 12)，完成老師倉庫的 fork，截圖並說明如何完成。

Ans:

我的做法如下：

1. 登入自己的 GitHub 帳號後，點選作業提供的連結，進入老師的倉庫頁面。
2. 點選頁面右上角的 **Fork** 按鈕。
3. 在 Owner 欄位選擇自己的帳號，倉庫名稱維持與老師相同，按下 **Create fork**。
4. 完成後，GitHub 會跳轉到 `https://github.com/uyennhile329-glitch/115-1HW1`，標題下方會出現「forked from 老師的倉庫」，代表 fork 成功。
5. 接著把自己帳號下的這份倉庫 clone 到本機，並用 VS Code 開啟：

```bash
git clone https://github.com/uyennhile329-glitch/115-1HW1.git
cd 115-1HW1
code .
```

fork 完成的截圖：

![fork 完成](images/1-fork.png)

clone 並用 VS Code 開啟的截圖：

![clone 完成](images/1-clone.png)


2. 請研究 markdown 基本寫作方法，並對常見語法進行介紹後，給個例子。

Ans:

Markdown 是一種輕量級標記語言，用簡單的符號就能表示標題、清單、連結等格式，之後可轉換成 HTML 或 PDF。GitHub 與 VS Code 都支援，所以很適合用來寫作業文件。

常見語法如下：

| 用途 | 語法 | 呈現結果 |
|---|---|---|
| 標題 | `# 一級標題`、`## 二級標題` | 不同層級的標題 |
| 粗體 | `**粗體**` | **粗體** |
| 斜體 | `*斜體*` | *斜體* |
| 刪除線 | `~~文字~~` | ~~文字~~ |
| 無序清單 | `- 項目` | 項目符號清單 |
| 有序清單 | `1. 項目` | 數字清單 |
| 連結 | `[文字](網址)` | [文字](https://github.com) |
| 圖片 | `![說明](圖片路徑)` | 顯示圖片 |
| 行內程式碼 | `` `code` `` | `code` |
| 程式碼區塊 | 三個反引號加語言名稱 | 帶語法色彩的程式區塊 |
| 引用 | `> 引用文字` | 縮排的引用區塊 |
| 分隔線 | `---` | 一條水平線 |

範例（原始碼）：

````markdown
# 遊戲開發筆記

今天學了 **Git** 與 *Markdown*。

## 待辦事項
1. Fork 老師的倉庫
2. 建立新分支
3. commit 並 push

- [Unity](https://unity.com)

> 常常 commit，每次改一點。

```bash
git status
```
````

範例（呈現結果）：

# 遊戲開發筆記

今天學了 **Git** 與 *Markdown*。

## 待辦事項
1. Fork 老師的倉庫
2. 建立新分支
3. commit 並 push

- [Unity](https://unity.com)

> 常常 commit，每次改一點。

```bash
git status
```

本檔案在 VS Code 預覽的截圖：

![markdown 預覽](images/2-markdown.png)


3. 請在你的專案中完成下面的操作，最後把結果推上 GitHub，並截圖 git graph 說明你的做法。

Ans:

**(i) 建立新分支**：先確認在 main 分支，再建立並切換到名為 `feature-112105142` 的新分支。

```bash
git checkout main
git checkout -b feature-112105142
```

![建立分支](images/3-i-branch.png)

**(ii) 新增檔案並寫入內容**：在新分支上新增 `hello.txt`，內容如下。

```text
Hello Git!
姓名：黎鴛兒
學號：112105142
```

![hello.txt](images/3-ii-file.png)

**(iii) 提交 (commit)**：把 `hello.txt` 加入暫存區再 commit，訊息寫明這次做了什麼。

```bash
git add hello.txt
git commit -m "新增 hello.txt"
```

![commit](images/3-iii-commit.png)

**(iv) 合併 (merge)**：切回 main，把新分支合併進來。

```bash
git checkout main
git merge feature-112105142
```

![merge](images/3-iv-merge.png)

**推上 GitHub**：

```bash
git push origin main
git push origin feature-112105142
```

**git graph 截圖**：

![git graph](images/3-graph.png)

從圖上可以看到 `feature-112105142` 分支從 main 分出去，在上面有一個「新增 hello.txt」的 commit，之後又合併回 main。


4. 請於「點我」找到自己的名字，並於「github帳號位址 [請撰寫]」欄位中貼上網址。

Ans:

做法：

1. 在 GitHub 右上角點選自己的頭像，選擇 **Profile**。
2. 複製進入 Profile 後網址列的網址，也就是 `https://github.com/uyennhile329-glitch`。
3. 回到老師提供的頁面，找到自己的名字（黎鴛兒），把網址貼到對應的「github帳號位址 [請撰寫]」欄位。

填寫結果截圖：

![填寫結果](images/4-profile.png)

## 其他

這次作業讓我實際操作了 fork、clone、分支與合併的完整流程，也第一次把 Markdown 轉成 PDF 並加上密碼保護。（可依自己的實際感想修改或補充。）
