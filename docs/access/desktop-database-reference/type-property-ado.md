---
title: Type (propiedad, ADO)
TOCTitle: Type Property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ac119b9582634e619455870c8a2e115f5e8dafa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484237"
---
# <a name="type-property-ado"></a><span data-ttu-id="17d6a-102">Type (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="17d6a-102">Type Property (ADO)</span></span>


<span data-ttu-id="17d6a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17d6a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17d6a-104">Indica el tipo operativo o tipo de datos de un objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) o [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="17d6a-104">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="17d6a-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="17d6a-105">Settings and Return Values</span></span>

<span data-ttu-id="17d6a-106">Establece o devuelve un valor de tipo [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="17d6a-106">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d6a-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17d6a-107">Remarks</span></span>

<span data-ttu-id="17d6a-p101">En objetos **Parameter**, la propiedad **Type** es de lectura y escritura. En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Type** sólo es de lectura y escritura después de que se haya especificado la propiedad [Value](value-property-ado.md) del objeto **Field** y el proveedor de datos haya agregado correctamente el nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="17d6a-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="17d6a-110">En el resto de los objetos, la propiedad **Type** es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="17d6a-110">For all other objects, the **Type** property is read-only.</span></span>
