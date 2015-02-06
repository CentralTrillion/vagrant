##安全軟體##

許多Docker入門教程會建議Windows或Mac用戶安裝[bootdocker](http://boot2docker.io/ "Title")。但基於以下理由，不採用這種方案:

  - boot2docker 會在你的電腦上安裝一台 [Tiny Core Linux](http://tinycorelinux.net/) 虛擬機，優點是輕薄短小，但缺點是，與實務常見的 Linux 生態嚴重脫節（實務上，哪些 server 會用 Tiny Core Linux？）。DevOps 觀念告訴我們，Dev 和 Ops 的環境愈接近，愈有利及早發現問題。
  
  - boot2docker 無法輕易做出獨立、可重複再現的組態，遑論多台主機的 cluster 實驗環境。

相較之下，Vagrant 方案則有下列好處：

  - 可直接在本機端模擬出伺服主機所採用的作業系統及組態，符合 DevOps 的最佳實務。
  
  - 可輕易做出獨立、可重複再現的多台主機 cluster 實驗環境，更可儲存組態快照 (snapshot)，不怕玩壞系統，可快速還原回原始設定。
  
  - 反正都要學一點新的東西，與其學習 boot2docker 獨有指令，不如學習用途更廣的 Vagrant。 

如果還不熟悉 Vagrant + VirtualBox 軟體組合，可以先閱讀以下不錯的\<Vagrant Tutorial\>系列文章。並請照著文中指示安裝軟體，並實際演練看看:

  1. [雲端研發人員，你也需要虛擬機！](http://www.codedata.com.tw/social-coding/vagrant-tutorial-1-developer-and-vm) ← 觀念
  2. [跟著流浪漢把玩虛擬機](http://www.codedata.com.tw/social-coding/vagrant-tutorial-2-playing-vm-with-vagrant) ← ★★ 軟體安裝，**至少這篇要照著做過一遍！** ★★
  3. [細說虛擬機生滅狀態](http://www.codedata.com.tw/social-coding/vagrant-tutorial-3-vm-lifecycle) ← 基本使用
  4. [虛擬機，若即若離的國中之國](http://www.codedata.com.tw/social-coding/vagrant-tutorial-4-guest-host-communication) ← 與主機互動
