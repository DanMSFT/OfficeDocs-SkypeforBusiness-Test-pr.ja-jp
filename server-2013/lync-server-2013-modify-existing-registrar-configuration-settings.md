﻿---
title: 既存のレジストラー構成設定の変更
TOCTitle: 既存のレジストラー構成設定の変更
ms:assetid: a8931511-3e66-49ed-a3ec-03bcd61ce1f0
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg182566(v=OCS.15)
ms:contentKeyID: 48273182
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 既存のレジストラー構成設定の変更

 

_**トピックの最終更新日:** 2012-11-01_

レジストラーを使用して、プロキシ サーバーの認証プロトコルを構成できます。 使用できるプロトコルの詳細については、「[レジストラー構成設定の作成](lync-server-2013-create-registrar-configuration-settings.md)」を参照してください。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>サーバーがリモートとエンタープライズ両方のクライアント認証をサポートする場合は、Kerberos と NTLM の両方を有効にすることをお勧めします。 エッジ サーバーと内部サーバーは通信して、NTLM 認証のみがリモート クライアントに提供されるようにします。 これらのサーバーで Kerberos のみが有効な場合、リモート ユーザーを認証できません。 エンタープライズ ユーザーはサーバーに対しても認証を行い、Kerberos が使用されます。</td>
</tr>
</tbody>
</table>


既存のレジストラーを変更するには、次の手順を実行します。

## 既存のレジストラーを変更するには

1.  RTCUniversalServerAdmins グループのメンバーである (または同等のユーザー権限を持つ) ユーザー アカウント、または CsServerAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、Lync Server 2013 を展開したネットワーク内の任意のコンピューターにログオンします。

2.  ブラウザー ウィンドウを開いて管理 URL を入力し、Lync Server コントロール パネルを開きます。Lync Server コントロール パネルを開くために使用できる他の方法の詳細については、「[Lync Server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」を参照してください。

3.  左側のナビゲーション バーで \[**セキュリティ**\] をクリックし、\[**レジストラー**\] をクリックします。

4.  \[**レジストラー**\] ページでサービスをクリックし、\[**編集**\] をクリックして、\[**詳細の表示**\] をクリックします。

5.  \[**レジストラー設定の編集**\] で、クライアントの機能や環境内のサポートに合わせて、次のうち 1 つまたは複数を選択します。
    
      - \[**Kerberos 認証を有効にする**\]。プール内のサーバーは、Kerberos 認証を使用してチャレンジを発行します。
    
      - \[**NTLM 認証を有効にする**\]。プール内のサーバーは、NTLM 認証を使用してチャレンジを発行します。
    
      - \[**証明書認証を有効にする**\]。プール内のサーバーは、クライアントに対して証明書を発行します。

6.  \[**確定**\] をクリックします。

