﻿---
title: 'Lync Server 2013: Active Directory への存続可能ブランチ アプライアンスの追加'
TOCTitle: Active Directory への存続可能ブランチ アプライアンスの追加
ms:assetid: 3e63507c-d60b-40ec-8bbe-586b1d707c3e
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg425906(v=OCS.15)
ms:contentKeyID: 48271859
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 での、Active Directory への存続可能ブランチ アプライアンスの追加

 

_**トピックの最終更新日:** 2012-09-23_

存続可能ブランチ アプライアンスを展開する予定がある場合は、Active Directory ドメイン サービスに 存続可能ブランチ アプライアンスを追加する必要があります。 中央サイトでこの手順を実行します。


> [!IMPORTANT]
> この手順は、存続可能ブランチ アプライアンスを展開している場合にのみ実行します。 この手順は、存続可能ブランチ サーバーを展開している場合には実行しないでください。



## 存続可能ブランチ アプライアンスを Active Directory ドメイン サービスに追加するには

1.  Enterprise Admins グループのメンバーとしてメンバー サーバーにログオンします。

2.  \[**スタート**\]、\[**管理ツール**\]、\[**Active Directory ユーザーとコンピューター**\] の順にクリックします。

3.  \[**操作**\] メニューの \[**新規**\] をクリックし、\[**コンピューター**\] をクリックします。

4.  \[**新しいオブジェクト - コンピューター**\] ダイアログ ボックスで、存続可能ブランチ アプライアンス コンピューター オブジェクトの名前 (BranchOffice1 など) を入力し、\[**変更**\] をクリックします。

5.  \[**ユーザーまたはグループの選択**\] ダイアログ ボックスで、RTCUniversalSBATechnicians グループを追加して \[**OK**\] をクリックします。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>ブランチ サイトの RTCUniversalSBATechnicians グループのメンバーが、後でこのデバイスをドメインに追加します。</td>
    </tr>
    </tbody>
    </table>


6.  \[**OK**\] をクリックして 存続可能ブランチ アプライアンス コンピューター オブジェクトを保存します。

7.  \[**スタート**\]、\[**管理ツール**\]、\[**ADSI Edit**\] の順にクリックします。

8.  \[**ADSI Edit**\] で、前のステップで作成したコンピューター オブジェクトを右クリックし、\[**プロパティ**\] をクリックします。

9.  属性リストで **servicePrincipalName** をクリックし、\[**編集**\] をクリックします。

10. **追加する値**フィールドに「HOST/\<SBA FQDN\>」と入力します。ここで、\<SBA FQDN\> は 存続可能ブランチ アプライアンスの完全修飾ドメイン名 (FQDN) です。 たとえば、**HOST/BranchOffice1.contoso.com** のように入力します。

11. \[**OK**\] をクリックして **servicePrincipalName** 属性の設定を保存し、\[**OK**\] をクリックしてコンピューター オブジェクトのプロパティを保存します。

12. \[**Active Directory ユーザーとコンピューター**\] で \[**ユーザー**\] を右クリックし、\[**新規作成**\] をクリックして \[**ユーザー**\] をクリックします。

13. ウィザードに情報を入力して 存続可能ブランチ アプライアンス技術者のドメイン ユーザー アカウントを作成します。

14. \[**Active Directory ユーザーとコンピューター**\] で \[**ユーザー**\] をクリックし、ユーザー オブジェクトを右クリックして \[**グループに追加**\] をクリックします。

15. \[**選択するオブジェクト名を入力してください**\] に **RTCUniversalSBATechnicians** と入力し、\[**OK**\] をクリックします。

16. ブランチ サイト技術者ごとに、ステップ 12 ～ 15 を繰り返します。

**次のステップ**: [Lync Server 2013 でのトポロジへのブランチ サイトの追加](lync-server-2013-add-branch-sites-to-your-topology.md)

