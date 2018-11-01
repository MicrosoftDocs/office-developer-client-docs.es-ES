---
title: Errores (referencia de escritorio de la base de datos de Access)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3908a4b882a78360d3fd30ede0d4b9e406d03be5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873883"
---
# <a name="errors"></a><span data-ttu-id="06f2e-102">Errores</span><span class="sxs-lookup"><span data-stu-id="06f2e-102">Errors</span></span>


<span data-ttu-id="06f2e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06f2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06f2e-p101">Toda operación que implique a objetos de ADO puede generar errores de proveedor. Cuando se produce alguno de estos errores, se colocan objetos **Error** en la colección **Errors** del objeto **Connection**. Para obtener detalles acerca del tratamiento de advertencias y errores en una aplicación de ADO, vea el [Capítulo 6: Tratamiento de errores](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="06f2e-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object. For details about handling warnings and errors in your ADO application, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="06f2e-p102">Los errores de aplicación pueden ser generados por un mecanismo independiente. Por ejemplo, en Visual Basic, el objeto **Err** contendrá errores de nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="06f2e-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

