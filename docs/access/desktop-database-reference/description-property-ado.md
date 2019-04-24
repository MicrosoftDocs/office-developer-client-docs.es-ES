---
title: DeScription (propiedad, ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293934"
---
# <a name="description-property-ado"></a><span data-ttu-id="fc04c-102">DeScription (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="fc04c-102">Description property (ADO)</span></span>


<span data-ttu-id="fc04c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc04c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc04c-104">Describe un objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fc04c-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc04c-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc04c-105">Return value</span></span>

<span data-ttu-id="fc04c-106">Devuelve un valor de tipo **String** que contiene una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="fc04c-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc04c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc04c-107">Remarks</span></span>

<span data-ttu-id="fc04c-p101">Use la propiedad **Description** para obtener una breve descripción del error. Muestre esta propiedad para alertar al usuario sobre un error que no puede o no desea controlar. La cadena procederá de ADO o de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="fc04c-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="fc04c-p102">Los proveedores son responsables de especificar el texto del error específico a ADO. ADO agrega un objeto [Error](error-object-ado.md) a la colección **Errors** por cada error o advertencia que recibe del proveedor. Enumere la colección **Errors** para rastrear los errores que especifica el proveedor.</span><span class="sxs-lookup"><span data-stu-id="fc04c-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

