---
title: Método Database. Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295026"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="6d013-102">Método Database. Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d013-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="6d013-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d013-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d013-104">Cierra un objeto **Database** abierto.</span><span class="sxs-lookup"><span data-stu-id="6d013-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d013-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d013-105">Syntax</span></span>

<span data-ttu-id="6d013-106">*expresión* . Close</span><span class="sxs-lookup"><span data-stu-id="6d013-106">*expression* .Close</span></span>

<span data-ttu-id="6d013-107">*expresión* Variable que representa un objeto **Database** .</span><span class="sxs-lookup"><span data-stu-id="6d013-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d013-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d013-108">Remarks</span></span>

<span data-ttu-id="6d013-109">Si el objeto **Database** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6d013-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="6d013-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="6d013-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

