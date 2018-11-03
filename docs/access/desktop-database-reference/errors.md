---
title: Errores (referencia de escritorio de la base de datos de Access)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f8514fddb5523b670e2dff2b9b55981cab52f72
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946989"
---
# <a name="errors"></a><span data-ttu-id="8d98b-102">Errores</span><span class="sxs-lookup"><span data-stu-id="8d98b-102">Errors</span></span>

<span data-ttu-id="8d98b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d98b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d98b-104">Toda operación que implique a objetos de ADO puede generar errores de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8d98b-104">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="8d98b-105">Cuando se produce alguno de estos errores, se colocan objetos **Error** en la colección **Errors** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="8d98b-105">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object.</span></span> <span data-ttu-id="8d98b-106">Para obtener información detallada sobre el tratamiento de advertencias y errores en una aplicación de ADO, vea [capítulo 6: tratamiento de errores](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8d98b-106">For details about handling warnings and errors in your ADO application, see [Chapter 6: Error handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="8d98b-p102">Los errores de aplicación pueden ser generados por un mecanismo independiente. Por ejemplo, en Visual Basic, el objeto **Err** contendrá errores de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="8d98b-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

