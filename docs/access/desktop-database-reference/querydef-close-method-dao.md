---
title: Método QueryDef.Close (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303307"
---
# <a name="querydefclose-method-dao"></a><span data-ttu-id="0fc74-102">Método QueryDef.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="0fc74-102">QueryDef.Close method (DAO)</span></span>


<span data-ttu-id="0fc74-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fc74-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fc74-104">Cierra un objeto **QueryDef** abierto.</span><span class="sxs-lookup"><span data-stu-id="0fc74-104">Closes an open **QueryDef**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc74-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fc74-105">Syntax</span></span>

<span data-ttu-id="0fc74-106">*expression* .Close</span><span class="sxs-lookup"><span data-stu-id="0fc74-106">*expression* .Close</span></span>

<span data-ttu-id="0fc74-107">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="0fc74-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fc74-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0fc74-108">Remarks</span></span>

<span data-ttu-id="0fc74-109">Si el objeto **QueryDef** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0fc74-109">If the **QueryDef** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="0fc74-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="0fc74-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

