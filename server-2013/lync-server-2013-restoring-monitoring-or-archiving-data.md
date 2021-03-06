﻿---
title: 監視データまたはアーカイブ データの復元
TOCTitle: 監視データまたはアーカイブ データの復元
ms:assetid: 60118526-13bb-4b03-803e-6ffae219d436
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Hh202175(v=OCS.15)
ms:contentKeyID: 52056603
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 監視データまたはアーカイブ データの復元

 

_**トピックの最終更新日:** 2013-02-18_

監視およびアーカイブ データを復元しなくても、障害発生後に Lync Server を起動して実行できます。ただし、監視データやアーカイブ データが組織にとって非常に重要な場合は、データベースの再作成後にそれらのデータを復元できます。

次の手順では、SQL Server Management Studio を使用してアーカイブ データまたは監視データを復元する方法を説明します。

## 監視データまたはアーカイブ データをバックアップ ファイルから復元するには

1.  ローカル コンピューターの Administrators グループまたは同等のユーザー権限を持つグループのメンバーとして、復元するサーバーに ログオンします。

2.  SQL Server Management Studio を開きます。そのためには、\[**スタート**\] ボタン、\[**すべてのプログラム**\] の順にクリックし、\[**Microsoft SQL Server 2012**\] または \[**Microsoft SQL Server 2008 R2**\] をクリックしてから \[**SQL Server Management Studio**\] をクリックします。

3.  \[**サーバーへの接続**\] で、少なくともサーバーの名前と認証情報を入力して SQL Server インスタンスに接続します。

4.  \[**オブジェクト エクスプローラー**\] で、\[**データベース**\] を右クリックし、\[**データベースの復元**\] をクリックします。

5.  \[**ページの選択**\] で \[**全般**\] をクリックし、\[**復元先データベース**\] でデータベース名を次のように選択します。
    
      - アーカイブ データベースの場合は、\[**LcsLog**\] を選択します。
    
      - 通話詳細記録 (CDR) データベースの場合は、\[**LcsCDR**\] を選択します。
    
      - Quality of Experience (QoE) データベースの場合は、\[**QoEMetrics**\] を選択します。

6.  \[**復元元デバイス**\] をクリックします。

7.  \[**復元するバックアップ セットの選択**\] で、バックアップ ファイルをクリックし、\[**復元**\] をクリックします。

8.  \[**ページの選択**\] で、\[**オプション**\] をクリックし、データ ファイルのパスとログのパスが適切なフォルダー内にあることを確認して、\[**OK**\] をクリックします。

## アクセス制御リスト (ACL) が適切なことを確認するには

1.  \[**データベース**\] を展開し、アーカイブ データベースまたは監視データベース、\[**セキュリティ**\]、\[**ユーザー**\] の順に展開します。

2.  ドメイン グループ RTCComponentUniversalServices がユーザーとして存在することを確認します。

3.  RTCComponentUniversalServices が \[**ユーザー**\] の下に存在しない場合は、次の操作を実行します。
    
    1.  \[**ユーザー**\] を右クリックし、\[**新しいユーザー**\] をクリックします。
    
    2.  \[**ログイン名**\] に必要なグループ名 (RTCComponentUniversalServices) を入力します。
    
    3.  \[**データベース ロールのメンバーシップ**\] で、\[**ServerRole**\] アクセス許可を選択し、\[**OK**\] をクリックします。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>アーカイブ サービスまたは監視サービスを再起動する必要はありません。</td>
    </tr>
    </tbody>
    </table>

