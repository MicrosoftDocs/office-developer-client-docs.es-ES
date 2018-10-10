---
title: DefinedSize (propiedad, ADO)
TOCTitle: DefinedSize Property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8ffd8bb24abcab737ebc4bb23a0af717c02d486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483897"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="1c498-102">DefinedSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="1c498-102">DefinedSize Property (ADO)</span></span>


<span data-ttu-id="1c498-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c498-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c498-104">Indica la capacidad de datos de un objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1c498-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c498-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c498-105">Return Value</span></span>

<span data-ttu-id="1c498-106">Devuelve un valor de tipo **Long** que refleja el tamaño definido de un campo como un número de bytes.</span><span class="sxs-lookup"><span data-stu-id="1c498-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c498-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c498-107">Remarks</span></span>

<span data-ttu-id="1c498-108">Utilice la propiedad **DefinedSize** para determinar la capacidad de datos de un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="1c498-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="1c498-p101">Las propiedades **DefinedSize** y [ActualSize](actualsize-property-ado.md) son diferentes. Por ejemplo, considere un objeto **Field** con un tipo declarado **adVarChar** y un valor de la propiedad **DefinedSize** de 50 que contenga un carácter único. El valor de la propiedad **ActualSize** que devuelve es la longitud del carácter único en bytes.</span><span class="sxs-lookup"><span data-stu-id="1c498-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

