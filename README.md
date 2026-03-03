# The Pareto-Minkowski Semiring of Hatsune Miku: How She Accidentally Invented $FL^{NL}$

[English Version](#english-version) | [正體中文版](#chinese-version)

<a name="english-version"></a>

This repository contains the LaTeX source code and associated assets for the paper submitted to **SIGBOVIK 2026**. 

## Abstract (Brief)
We revisit the score maximization problem in an arcade rhythm game: Hatsune Miku: Project DIVA Arcade (PDA), previously argued in a companion manuscript to be polynomial-time solvable and to lie in $NC^2$ via parallel transfer-function composition. We observe that the underlying computation possesses a natural algebraic structure: the set of Pareto frontiers over non-negative integer pairs forms a semiring, specifically an additively idempotent semiring (dioid), under union-then-Pareto-prune as addition and Minkowski-sum-then-Pareto-prune as multiplication.
We call this the Pareto-Minkowski semiring (or, in honour of its application domain, the Hatsune semiring). Under this lens, the transfer-function composition becomes iterated matrix multiplication over a semiring, directly connecting rhythm game optimization to the classical theory of algebraic path problems. We further refine the complexity classification by showing that the decision version lies in NL and the search version in $FL^{NL}$, obtaining the tighter upper bound of NL within $NC^2$. These results demonstrate that SEGA's scoring system, while appearing fiendishly complex to players, inhabits a remarkably well-studied algebraic and complexity-theoretic landscape.

> "There is no excuse to name an algebraic structure after a #39c5bb-haired virtual singer, ...unless it yields an efficient parallel algorithm."

---

## Technical Specifications

This project is designed for a standard TeX Live environment. 

### 1. Typography & Fonts
* **Main Typeface**: Linux Libertine (via `\usepackage{libertine}`).
* **CJK Support**: Handled by the `CJKutf8` package.
    * **Traditional Chinese**: `bsmi` family.
    * **Japanese**: `min` family.
* **Requirements**: No external `.otf` or `.ttf` files are necessary as long as the TeX distribution includes the standard `libertine` and `latex-cjk-all` packages.

### 2. Core Algebraic Identity
The optimality of the dynamic programming approach relies on the following factoring identity:
$$\text{Pareto}(X +_M Y) = \text{Pareto}(\text{Pareto}(X) +_M Y)$$

### 3. Empirical Data (The Mystery of the Gap)
Visual evidence was captured from a public YouTube livestream of a local arcade session. 
* **Note**: Although the manuscript characterizes the source as a '24-hour livestream', empirical observation reveals a consistent **~90-minute enigmatic void** (approx. 22.5 hours of uptime) occurring daily during the nocturnal phase. The cause of this temporal discontinuity remains unknown.

---

## Build Instructions

To reproduce the final PDF, please use the following compilation recipe:

```bash
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex
```

## License & Attribution

* **Research Content & Code**: © 2026 The Author.
* **Game Assets**: User interface elements and character models from Hatsune Miku: Project DIVA Arcade are the property of SEGA and Crypton Future Media, INC..
* **Fair Use Notice**: These assets are included strictly for academic analysis and illustrative purposes under Fair Use guidelines.


---


<a name="chinese-version"></a>

## 摘要
我們重新審視了大型電玩節奏遊戲《初音未來 Project DIVA Arcade》（PDA）中的得分最大化問題。先前在相關手稿中曾論證該問題具有多項式時間可解性，且能透過平行轉移函數組合歸類於 $NC^2$ 複雜度類別。我們觀察到其底層計算具備一種天然的代數結構：非負整數對上的帕雷托前沿（Pareto frontiers）集合，在「聯集後進行Pareto剪枝」作為加法，以及「閔可夫斯基和（Minkowski sum）後進行Pareto剪枝」作為乘法的運算下，構成了一個半環（semiring），具體而言是一個加法冪等半環（additively idempotent semiring，即dioid）。我們將其稱為「Pareto-Minkowski半環」（或為了向其應用領域致敬，稱之為初音半環Hatsune semiring）。在此視角下，轉移函數的組合轉化為半環上的矩陣鏈乘法，直接將節奏遊戲的最佳化問題與代數路徑問題（algebraic path problems）的古典理論聯繫起來。我們進一步細化了複雜度分類，證明其判定版本（decision version）屬於 $NL$，而搜尋版本（search version）屬於 $FL^{NL}$，從而在 $NC^2$ 之內獲得了更緊緻的 $NL$ 上界。這些結果顯示，儘管SEGA的計分系統對玩家而言看似極度複雜，但其實際上處於一個研究極為透徹的代數與複雜度理論範疇之中。

> 「要不是它能產生高效的平行演算法，誰會想用 #39c5bb 髮色的車欠骨豊來幫代數結構取名？」

---

## 技術規格

本專案設計運行於標準TeX Live環境。

### 1. 字型及排版
* **主要字型**: Linux Libertine (以`\usepackage{libertine}`引用).
* **CJK支援**: 由 `CJKutf8` 套件處理。包含：
    * **正體中文**: `bsmi`。
    * **日文**: `min`。
* **需求**: 只要TeX發行版包含標準的`libertine`和`latex-cjk-all`巨集包，就不需要外部的`.otf`或`.ttf`檔案。

### 2. 核心代數恆等式
動態規劃方法的最適性依賴以下因式分解恆等式：
$$\text{Pareto}(X +_M Y) = \text{Pareto}(\text{Pareto}(X) +_M Y)$$

### 3. 實證資料（時間差之謎）

我們從YouTube上公開的遊戲直播中取得影片證據。
* **附註**：雖然我們的論文稿寫這是「24小時直播」，但實際上在凌晨時段，每天都會出現約90分鐘的神秘空白期（所以總共直播約22.5小時），原因仍然未知。

---

## Build Instructions

編譯指令請在具備TeX Live環境的終端機執行：

```bash
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex
```

---

## 版權聲明（License）
* **研究內容與程式碼**：© 2026 作者。
* **遊戲資產**：「初音未來 Project DIVA Arcade」之UI與角色模組版權等歸SEGA及Crypton Future Media, INC.所有。
* **合理使用聲明**：本研究基於學術分析目的進行合理使用。