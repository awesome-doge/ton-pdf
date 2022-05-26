# 5. TON Payments

我們將在本文TON 項目的最後一部分簡要討論TON Payments，這是（小額）支付通道和“閃電網路”價值轉移的平臺。它將實現“即時”支付，無需將所有交易提交到區塊鏈中、支付相關的交易費用（例如消耗的 gas）並等待五秒鐘、直到確認包含有關交易的區塊。
這種即時支付的總體開銷很小，可以將它們用於小額支付。例如，TON file-storing 服務可能會為每下載 128 KiB向用戶收費，或者付費 TON 代理可能需要為轉發的每128 KiB提供一些小額微支付。
雖然 TON Payments 可能會晚於 TON 專案核心部分的發佈，但一開始就需要考慮這些因
素。例如，用於執行 TON區塊鏈智能合約代碼的 TON 虛擬機器（TON VM；參見 2.1.20）必須
支持默克爾校驗的一些特殊操作。如果最初的設計中不存在此類支持，在之後的階段添加則可

能會出現問題（參見 2.8.16）。但是，我們將看到 TON虛擬機器天然支持“智慧”支付通道（參
見 5.1.9）。