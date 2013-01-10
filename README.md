EPUBConverter 0.0.2
-------------------------------------------------------------

一開始的 Scala 版本本來是自己寫來自己用的小工具，可是沒想到竟然有人有用還有回報問題。
大受感動之餘（誤），而出現了這個全新感受的 EPUBConverter 0.0.2，絕對不是因為手癢想要試試看 Go。

P.S 2012.12.09 更新 - 修正了鳥 Bug 所以到 0.0.3 了。

`EPUBConverter 0.0.3 下載`_

`EPUBConverter Source Code`_

這個版本比之前好得地方在於，這次使用了 新同文堂_ 的簡繁轉換對照表。
除了單字轉換之外，還多了一個詞彙轉換。

所以轉換品質應該會比之前 Scala 的版本好很多，感謝新同文堂分享對照表。
他的 Bookmarklet 版本也非常好用，基本上我 Go 的轉換邏輯就是從 Bookmarklet 版本移植過來的。

但是由於我直接將對照表轉換成 Golang 裡面的 map 了，所以這次就沒有辦法讓使用者自己改對照表了。

不過有興趣的人，在原始碼的 tongwen_table_ 資料夾底下，我有放了一個簡單的轉換工具。
可以利用那個重新產生 Go 的 map，但是最後還是得重新編譯整個 EPUBConverter 就是了。

延續之前的我的偷懶寫法，這次也是寫死只會轉換 source 資料夾底下的 epub 檔案，輸出到 target 資料夾。
可是這次全部都在記憶體裡面處理，所以不會先解壓縮到磁碟上然後壓縮再刪除了。

::

  /EPUBConverter
		   source
  		   target
  		   epubconverter.exe

以上，如果有什麼問題的話也歡迎回覆，如果我有錢有閒而且沒事做的話 Orz。
會找個時間繼續修正的，雖然目前我也想不到要加啥功能。

.. _EPUBCOnverter 0.0.3 下載: https://dl.dropbox.com/u/15537823/EPUBConverter_0.0.3.7z
.. _EPUBConverter Source Code: https://github.com/Swind/EPUBConverter-Go
