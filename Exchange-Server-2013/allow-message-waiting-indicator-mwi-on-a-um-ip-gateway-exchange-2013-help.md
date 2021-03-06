﻿---
title: '允許郵件等待指示器 (MWI) 上的 UM IP 閘道: Exchange Online Help'
TOCTitle: 允許郵件等待指示器 (MWI) 上的 UM IP 閘道
ms:assetid: 5667e37c-48c6-4659-9dc9-94b1dd8ba232
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Dd297995(v=EXCHG.150)
ms:contentKeyID: 50473236
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 允許郵件等待指示器 (MWI) 上的 UM IP 閘道

 

_**適用版本：** Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**上次修改主題的時間：** 2013-02-23_

您可以允許或防止使用者接收到的整合通訊 (UM) IP 閘道的電話語音信箱簡訊通知。如果您啟用此設定，UM IP 閘道可接收及傳送 SIP 通知訊息的使用者。訊息等待指示器 (MWI) 預設會啟用，並允許郵件等待將通知傳送給使用者，但您可以將它關閉視您的需求而定。

訊息等待指示器會通知使用者關於新的或技術面貌語音訊息。它會出現在用戶端如 Outlook 和 Outlook Web App 中的收件匣。它也可以是文字 (SMS) 訊息傳送到已登錄的行動電話，從 Exchange 伺服器對已設定為使用者的桌上電話上播放新郵件或 lighted 的燈號碼的撥出電話。


> [!TIP]  
> 您也可以在 UM 信箱原則上針對使用者群組啟用和停用 MWI 通知。




如需與 UM IP 閘道相關的其他管理工作，請參閱[UM IP 閘道程序](um-ip-gateway-procedures-exchange-2013-help.md)。

## 開始之前有哪些須知？

  - 預估完成時間： 少於 1 分鐘。

  - 您必須已獲指派權限，才能執行此程序或這些程序。若要查看您需要的權限，請參閱 [整合的通訊權限](unified-messaging-permissions-exchange-2013-help.md)主題中的「UM IP 閘道」項目。

  - 在執行這些程序之前，請確認已建立 UM 撥號對應表。如需詳細步驟，請參閱[建立 UM 撥號對應表](create-a-um-dial-plan-exchange-2013-help.md)。

  - 執行這些程序之前，請確認已建立 UM IP 閘道器。如需詳細步驟，請參閱[建立 UM IP 閘道器](create-a-um-ip-gateway-exchange-2013-help.md)。

  - 如需適用於此主題中程序的快速鍵相關資訊，請參閱 [Exchange 系統管理中心的鍵盤快速鍵](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md)。


> [!TIP]  
> 有問題嗎？在 Exchange 論壇中尋求協助。 論壇的網址為：<a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>、 <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a> 或 <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>。.




## 您要執行的工作

## 使用 EAC 以允許訊息等待指示器

1.  在 EAC 中，瀏覽至 \[整合通訊\] \> \[UM IP 閘道\]，選取要變更的 UM IP 閘道，然後按一下 \[編輯\]![編輯圖示](images/JJ218640.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "編輯圖示")。

2.  在 \[UM IP 閘道\]**UM IP Gateway** 頁面，選取 \[允許訊息等待指示器\]旁的勾選方塊。

3.  按一下 \[儲存\]。

## 使用命令介面可允許訊息等待指示器

此範例允許訊息等待指示器向與名為 `MyUMIPGateway` IP 位址為 10.10.10.1 的 UM IP 閘道關聯的使用者顯示。

    Set-UMIPGateway -Identity MyUMIPGateway -Address 10.10.10.1 -MessageWaitingIndicatorAllowed $true

