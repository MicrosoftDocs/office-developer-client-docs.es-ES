---
title: Errores (referencia de base de datos de escritorio de Access)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 056ec0b34991348728898b4c0fc4a1a516a9913f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293360"
---
# <a name="errors"></a><span data-ttu-id="3f4e7-102">Errores</span><span class="sxs-lookup"><span data-stu-id="3f4e7-102">Errors</span></span>

<span data-ttu-id="3f4e7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f4e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f4e7-104">Toda operación que implique a objetos de ADO puede generar errores relacionados con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-104">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="3f4e7-105">Cuando se produce alguno de estos errores, se colocan objetos **Error** en la colección **Errors** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-105">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object.</span></span> <span data-ttu-id="3f4e7-106">Para obtener información detallada sobre el tratamiento de advertencias y errores en una aplicación de ADO, vea el [capítulo 6: tratamiento de errores](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="3f4e7-106">For details about handling warnings and errors in your ADO application, see [Chapter 6: Error handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="3f4e7-p102">Los errores de aplicación pueden ser generados por un mecanismo independiente. Por ejemplo, en Visual Basic, el objeto **Err** contendrá errores de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f4e7-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

