---
title: Database.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97246da6224ee04fa435638a0cb11d1bdac8859f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484047"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="d2a31-102">Database.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2a31-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="d2a31-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2a31-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2a31-104">Cierra un objeto **Database** abierto.</span><span class="sxs-lookup"><span data-stu-id="d2a31-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a31-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2a31-105">Syntax</span></span>

<span data-ttu-id="d2a31-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="d2a31-106">*expression* .Close</span></span>

<span data-ttu-id="d2a31-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="d2a31-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a31-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2a31-108">Remarks</span></span>

<span data-ttu-id="d2a31-109">Si el objeto **Database** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d2a31-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="d2a31-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="d2a31-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

