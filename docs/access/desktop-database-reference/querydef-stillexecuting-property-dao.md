---
title: Propiedad QueryDef.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303419"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="4ebf8-102">Propiedad QueryDef.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ebf8-102">QueryDef.StillExecuting property (DAO)</span></span>


<span data-ttu-id="4ebf8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ebf8-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebf8-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ebf8-104">Syntax</span></span>

<span data-ttu-id="4ebf8-105">*expresión* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="4ebf8-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="4ebf8-106">*expression* Variable que representa un objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4ebf8-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebf8-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ebf8-107">Remarks</span></span>

<span data-ttu-id="4ebf8-p101">Use la propiedad **StillExecuting** para determinar si el método asincrónico **[Execute](querydef-execute-method-dao.md)** o **[OpenConnection](dbengine-openconnection-method-dao.md)** invocado más recientemente (es decir, un método ejecutado con la opción **dbRunAsync**) se completó. Mientras la propiedad **StillExecuting** esté establecida en **True**, no se puede tener acceso a ningún objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="4ebf8-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="4ebf8-p102">Una vez que la propiedad **StillExecuting** devuelva **False**, seguido de la llamada **OpenConnection** que devuelve el objeto asociado **[Connection](connection-object-dao.md)**, se puede hacer referencia al objeto. Mientras que **StillExecuting** permanezca establecida en **True**, no se puede hacer referencia al objeto, aparte de leer la propiedad **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="4ebf8-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="4ebf8-112">Utilice el método **[Cancel](connection-cancel-method-dao.md)** para finalizar la ejecución de una tarea que se esté realizando.</span><span class="sxs-lookup"><span data-stu-id="4ebf8-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

