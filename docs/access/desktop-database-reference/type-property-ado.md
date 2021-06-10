---
title: Propiedad Type (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314017"
---
# <a name="type-property-ado"></a><span data-ttu-id="c1bdd-102">Propiedad Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="c1bdd-102">Type property (ADO)</span></span>


<span data-ttu-id="c1bdd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1bdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1bdd-104">Indica el tipo operativo o tipo de datos de un objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) o [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1bdd-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c1bdd-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c1bdd-105">Settings and return values</span></span>

<span data-ttu-id="c1bdd-106">Establece o devuelve un valor de tipo [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="c1bdd-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1bdd-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1bdd-107">Remarks</span></span>

<span data-ttu-id="c1bdd-p101">En objetos **Parameter**, la propiedad **Type** es de lectura y escritura. En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Type** sólo es de lectura y escritura después de que se haya especificado la propiedad [Value](value-property-ado.md) del objeto **Field** y el proveedor de datos haya agregado correctamente el nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="c1bdd-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="c1bdd-110">En el resto de los objetos, la propiedad **Type** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1bdd-110">For all other objects, the **Type** property is read-only.</span></span>

