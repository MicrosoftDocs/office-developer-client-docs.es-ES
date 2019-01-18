---
title: QueryDef.Close (método) (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720005"
---
# <a name="querydefclose-method-dao"></a><span data-ttu-id="cf037-102">QueryDef.Close (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="cf037-102">QueryDef.Close method (DAO)</span></span>


<span data-ttu-id="cf037-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf037-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf037-104">Cierra un objeto **QueryDef** abierto.</span><span class="sxs-lookup"><span data-stu-id="cf037-104">Closes an open **QueryDef**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf037-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf037-105">Syntax</span></span>

<span data-ttu-id="cf037-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="cf037-106">*expression* .Close</span></span>

<span data-ttu-id="cf037-107">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="cf037-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf037-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf037-108">Remarks</span></span>

<span data-ttu-id="cf037-109">Si el objeto **QueryDef** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cf037-109">If the **QueryDef** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="cf037-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="cf037-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

