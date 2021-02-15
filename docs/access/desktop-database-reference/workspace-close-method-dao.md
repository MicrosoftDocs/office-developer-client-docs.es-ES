---
title: Método Workspace.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305960"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="4b4b2-102">Método Workspace.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b4b2-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="4b4b2-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b4b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b4b2-104">Cierra un objeto **Workspace** abierto.</span><span class="sxs-lookup"><span data-stu-id="4b4b2-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b4b2-105">Syntax</span></span>

<span data-ttu-id="4b4b2-106">*expression* .Close</span><span class="sxs-lookup"><span data-stu-id="4b4b2-106">*expression* .Close</span></span>

<span data-ttu-id="4b4b2-107">*expression* Variable que representa un objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="4b4b2-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b4b2-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b4b2-108">Remarks</span></span>

<span data-ttu-id="4b4b2-109">Si el objeto **Workspace** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4b4b2-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="4b4b2-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="4b4b2-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

