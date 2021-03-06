﻿---
title: 'Lync Server 2013: 常設チャット サーバー ポリシーを有効にする'
TOCTitle: 常設チャット サーバー ポリシーを有効にする
ms:assetid: 87063d6c-2e38-4970-b76d-2aa15f0de29e
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ205056(v=OCS.15)
ms:contentKeyID: 48272782
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 で常設チャット サーバー ポリシーを有効にする

 

_**トピックの最終更新日:** 2012-10-06_

Lync Server 2013 コントロール パネルでは、\[**常設チャット**\] グループの \[**常設チャット ポリシー**\] ページを使用して、グローバル、プール、サイト、またはユーザー レベルで、既定のグローバル ポリシーの構成、1 つ以上の追加ユーザーの作成、ユーザーの展開用のサイト ポリシーの作成など、ポリシー管理を実行できます。ポリシーによりユーザーが 常設チャット サーバーに対して有効な場合、常設チャット サーバー環境がユーザーの Lync 2013 クライアントに表示されます。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>トポロジでは、常設チャット サーバー サイト ポリシーは、グローバルに、ユーザーのプールごとに、ユーザーのサイトごとに、またはユーザーごとに適用されます。</td>
</tr>
</tbody>
</table>


グローバル ポリシーは、常設チャット サーバーを展開するときに自動的に作成および構成できますが、削除することはできません。グローバル ポリシーはすべてのユーザーに適用されるため、ユーザーごとに設定する必要はありません。

複数のサイト ポリシーとユーザー ポリシーを作成および構成できます。これらのポリシーはグローバル ポリシーと連携して、常設チャット サーバーのユーザーを有効にします。プールおよびサイトの 常設チャット サーバー ポリシーは、グローバルな 常設チャット サーバー ポリシーよりも優先されますが、対象となるのは、そのサイトのユーザーのみです。ユーザー ポリシーは、そのユーザー ポリシーが割り当てられているユーザーに対しては、グローバル、プール、およびサイト ポリシーよりも優先されます。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>常設チャット サーバーを構成して使用するには、まず、トポロジ ビルダーを使用して 常設チャット サーバー サポートをトポロジに追加してから、そのトポロジを公開する必要があります。詳細については、「展開」のドキュメントの「<a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Lync Server 2013 での展開への常設チャットサーバーの追加</a>」を参照してください。</td>
</tr>
</tbody>
</table>


## このセクション中

  - [Lync Server 2013 で常設チャットのグローバル ポリシーを構成する](lync-server-2013-configure-the-global-policy-for-persistent-chat.md)

  - [Lync Server 2013 で常設チャットのサイト ポリシーを作成する](lync-server-2013-create-a-site-policy-for-persistent-chat.md)

  - [Lync Server 2013 で常設チャット用のユーザー ポリシーを作成する](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

  - [Lync Server 2013 で常設チャット ポリシーをユーザーまたはユーザー グループに適用する](lync-server-2013-apply-a-persistent-chat-policy-to-a-user-or-user-group.md)

