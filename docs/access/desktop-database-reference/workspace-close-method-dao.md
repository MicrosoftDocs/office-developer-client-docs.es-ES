---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87f72a58cd3e24838416ef4d19ec1a2cf91e7c1f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483918"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="e99d1-102">Workspace.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="e99d1-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="e99d1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e99d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e99d1-104">Cierra un objeto **Workspace** abierto.</span><span class="sxs-lookup"><span data-stu-id="e99d1-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e99d1-105">Syntax</span></span>

<span data-ttu-id="e99d1-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="e99d1-106">*expression* .Close</span></span>

<span data-ttu-id="e99d1-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="e99d1-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e99d1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e99d1-108">Remarks</span></span>

<span data-ttu-id="e99d1-109">Si el objeto **Workspace** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e99d1-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="e99d1-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="e99d1-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

