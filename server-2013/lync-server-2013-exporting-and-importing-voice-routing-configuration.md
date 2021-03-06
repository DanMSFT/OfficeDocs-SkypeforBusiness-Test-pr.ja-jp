﻿---
title: 'Lync Server 2013: 音声ルーティング構成のエクスポートとインポート'
TOCTitle: 音声ルーティング構成のエクスポートとインポート
ms:assetid: c9b78622-5725-43b0-9ee1-5b82b1e1c8eb
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg398836(v=OCS.15)
ms:contentKeyID: 48273591
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 での音声ルーティング構成のエクスポートとインポート

 

_**トピックの最終更新日:** 2012-11-01_

音声ルーティング構成を公開せずに保存する場合、この手順を実行して、Lync Server コントロール パネルの構成のエクスポート コマンドおよびインポート コマンドを使用し、音声ルーティング構成のスナップショットを保存して取得します。音声ルーティング構成ファイル (.vcfg) をインポートするまでに、サーバーで音声ルーティング構成が変更されていた場合、Lync Server コントロール パネルの \[**音声ルーティング**\] グループの各種ページで、音声ルーティングに未確定の変更があることが表示されます。これらの未確定の変更は、調整が必要な 2 つの構成間の相違です。


> [!IMPORTANT]
> [<STRONG>音声ルーティング</STRONG>] グループ内のいずれかのページで、設定に対して未確定の変更を行った場合、これらの変更はエクスポートされた音声構成ファイル (.vcfg) に保存されます。このことにより、変更を公開する前に、複数の Lync Server コントロール パネル セッションで音声ルーティング構成を変更できます。



## このセクション中

  - [Lync Server 2013 でのボイス ルート構成ファイルのエクスポート](lync-server-2013-export-a-voice-route-configuration-file.md)

  - [Lync Server 2013 でのボイス ルート構成ファイルのインポート](lync-server-2013-import-a-voice-route-configuration-file.md)

## 関連項目

