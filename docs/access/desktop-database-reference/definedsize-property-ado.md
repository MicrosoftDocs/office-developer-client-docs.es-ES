---
title: Propiedad DefinedSize (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294137"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="44d2c-102">Propiedad DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="44d2c-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="44d2c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44d2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44d2c-104">Indica la capacidad de datos de un objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44d2c-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="44d2c-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44d2c-105">Return value</span></span>

<span data-ttu-id="44d2c-106">Devuelve un valor de tipo **Long** que refleja el tamaño definido de un campo como un número de bytes.</span><span class="sxs-lookup"><span data-stu-id="44d2c-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d2c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44d2c-107">Remarks</span></span>

<span data-ttu-id="44d2c-108">Utilice la propiedad **DefinedSize** para determinar la capacidad de datos de un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="44d2c-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="44d2c-p101">Las propiedades **DefinedSize** y [ActualSize](actualsize-property-ado.md) son diferentes. Por ejemplo, considere un objeto **Field** con un tipo declarado **adVarChar** y un valor de la propiedad **DefinedSize** de 50 que contenga un carácter único. El valor de la propiedad **ActualSize** que devuelve es la longitud del carácter único en bytes.</span><span class="sxs-lookup"><span data-stu-id="44d2c-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

