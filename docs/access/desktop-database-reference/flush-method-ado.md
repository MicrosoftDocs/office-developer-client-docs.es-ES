---
title: Flush (método) - ActiveX Data Objects (ADO)
TOCTitle: Flush Method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3c2d7543d2e9a1229661e572e95b783621aa43fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486234"
---
# <a name="flush-method-ado"></a><span data-ttu-id="14277-102">Flush (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="14277-102">Flush Method (ADO)</span></span>


<span data-ttu-id="14277-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="14277-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="14277-104">Vuelca el contenido del objeto [Stream](stream-object-ado.md) que queda en el búfer de ADO en el objeto subyacente al que está asociado el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="14277-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="14277-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14277-105">Syntax</span></span>

<span data-ttu-id="14277-106">*Secuencia*. Vaciar</span><span class="sxs-lookup"><span data-stu-id="14277-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="14277-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14277-107">Remarks</span></span>

<span data-ttu-id="14277-p101">Este método puede utilizarse para enviar el contenido del búfer de secuencia al objeto subyacente (por ejemplo, el nodo o archivo representado por la dirección URL que es el origen del objeto **Stream** ). Este método debe invocarse cuando se desea garantizar que se hayan escrito todos los cambios realizados en el contenido de un objeto **Stream**. Sin embargo, con ADO, normalmente no es necesario llamar a **Flush**, puesto que ADO vacía continuamente y en la medida de lo posible su búfer en segundo plano. Los cambios en el contenido de un objeto **Stream** se realizan automáticamente y no se almacenan en la memoria caché hasta que se llama al método **Flush**.</span><span class="sxs-lookup"><span data-stu-id="14277-p101">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object). This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written. However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background. Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="14277-112">Si se cierra un objeto **Stream** con el método [Close](close-method-ado.md), se vacía automáticamente el contenido del objeto **Stream**; no es necesario llamar explícitamente a **Flush** inmediatamente antes de llamar a **Close**.</span><span class="sxs-lookup"><span data-stu-id="14277-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

