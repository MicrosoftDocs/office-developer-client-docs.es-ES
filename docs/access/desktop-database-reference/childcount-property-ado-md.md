---
title: Propiedad ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f8e0fc98d7868eb5462bd7d8714e1a8eda1cfcf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296384"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="976c0-102">Propiedad ChildCount (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="976c0-102">ChildCount property (ADO MD)</span></span>


<span data-ttu-id="976c0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="976c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="976c0-104">Indica el número de elementos para los que el objeto [Member](member-object-ado-md.md) activo es el principal en una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="976c0-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="976c0-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="976c0-105">Return values</span></span>

<span data-ttu-id="976c0-106">Devuelve un entero **Long** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="976c0-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="976c0-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="976c0-107">Remarks</span></span>

<span data-ttu-id="976c0-p101">Use la propiedad **ChildCount** para devolver una estimación del número de elementos secundarios que tiene un objeto **Member**. Los elementos secundarios de un objeto **Member** se pueden obtener mediante la propiedad [Children](children-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="976c0-p101">Use the **ChildCount** property to return an estimate of how many children a **Member** has. The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="976c0-p102">Para objetos **Member** a partir de un objeto [Position](position-object-ado-md.md), el máximo valor que se puede devolver es 65.536. Si la cantidad real de elementos secundarios es mayor que 65.536, el valor devuelto seguirá siendo 65.536. Por tanto, la aplicación debería interpretar un valor **ChildCount** de 65.536 como que existe esta cantidad o más de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="976c0-p102">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536. If the actual number of children exceeds 65536, the value returned will still be 65536. Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="976c0-p103">Para objetos **Member** a partir de un objeto [Level](level-object-ado-md.md), utilice la propiedad [Contar](count-property-ado.md) de la colección de ADO con la colección **Children** para determinar el número exacto de elementos secundarios. La determinación del número exacto de elementos secundarios puede requerir su tiempo si la cantidad de secundarios en la colección es elevada.</span><span class="sxs-lookup"><span data-stu-id="976c0-p103">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children. Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

