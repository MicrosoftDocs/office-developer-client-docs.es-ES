---
title: Close (método, ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 609069d04124146f311166e3ae56d8d6a793675b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709834"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="b3d06-102">Close (método, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b3d06-102">Close method (ADO MD)</span></span>


<span data-ttu-id="b3d06-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3d06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3d06-104">Cierra un conjunto de celdas abierto.</span><span class="sxs-lookup"><span data-stu-id="b3d06-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d06-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3d06-105">Syntax</span></span>

<span data-ttu-id="b3d06-106">*Conjunto de celdas*. Cerrar</span><span class="sxs-lookup"><span data-stu-id="b3d06-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d06-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3d06-107">Remarks</span></span>

<span data-ttu-id="b3d06-p101">Si se usa el método **Close** para cerrar un objeto [Cellset](cellset-object-ado-md.md), se liberarán los datos asociados, incluidos los datos de todo objeto [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) o [Member](member-object-ado-md.md) relacionado. El hecho de cerrar un **conjunto de celdas** no lo borra de la memoria; puede cambiar la configuración de sus propiedades y abrirlo de nuevo más tarde. Para eliminar completamente un objeto de la memoria, establezca la variable del objeto en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="b3d06-p101">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects. Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later. To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="b3d06-p102">Puede llamar posteriormente al método [Open](open-method-ado-md.md) para volver a abrir el **conjunto de celdas** utilizando la misma cadena de origen u otra. Si, mientras se cierra el objeto **Cellset**, se recuperan propiedades o se llama a algún método que haga referencia a los datos o metadatos subyacentes, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b3d06-p102">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string. While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

