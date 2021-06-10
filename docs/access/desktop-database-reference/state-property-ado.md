---
title: Propiedad State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308536"
---
# <a name="state-property-ado"></a><span data-ttu-id="8ea16-102">Propiedad State (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ea16-102">State property (ADO)</span></span>


<span data-ttu-id="8ea16-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ea16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ea16-104">Indica, para todos los objetos aplicables, si el estado del objeto es abierto o cerrado.</span><span class="sxs-lookup"><span data-stu-id="8ea16-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="8ea16-105">Indica para todos los objetos aplicables que ejecutan un método asincrónico si el objeto se encuentra actualmente en estado de conexión, ejecución o recuperación.</span><span class="sxs-lookup"><span data-stu-id="8ea16-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ea16-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ea16-106">Return value</span></span>

<span data-ttu-id="8ea16-p101">Devuelve un valor de tipo **Long** que puede ser un valor [ObjectStateEnum](objectstateenum.md). El valor predeterminado es **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="8ea16-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea16-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ea16-109">Remarks</span></span>

<span data-ttu-id="8ea16-110">Puede utilizar la propiedad **Estado (State)** para determinar el estado actual de un objeto dado en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="8ea16-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="8ea16-p102">La propiedad **Estado (State)** del objeto puede tener una combinación de valores. Por ejemplo, si se está ejecutando una instrucción, esta propiedad tendrá un valor combinado de **adStateOpen** y **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="8ea16-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="8ea16-113">La propiedad **Estado (State)** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ea16-113">The **State** property is read-only.</span></span>

