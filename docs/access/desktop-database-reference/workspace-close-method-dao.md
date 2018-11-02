---
title: Workspace.Close (método) (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63b935fa178eb4c55ce11724ec3fd5f62d056779
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919853"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="9e2c5-102">Workspace.Close (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e2c5-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="9e2c5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e2c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e2c5-104">Cierra un objeto **Workspace** abierto.</span><span class="sxs-lookup"><span data-stu-id="9e2c5-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e2c5-105">Syntax</span></span>

<span data-ttu-id="9e2c5-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="9e2c5-106">*expression* .Close</span></span>

<span data-ttu-id="9e2c5-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="9e2c5-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e2c5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e2c5-108">Remarks</span></span>

<span data-ttu-id="9e2c5-109">Si el objeto **Workspace** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9e2c5-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="9e2c5-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="9e2c5-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

