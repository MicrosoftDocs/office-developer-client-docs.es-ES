---
title: NumericScale (propiedad, ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288556"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="5b08e-102">NumericScale (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="5b08e-102">NumericScale property (ADO)</span></span>


<span data-ttu-id="5b08e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b08e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b08e-104">Indica la escala de valores numéricos de un objeto [Parameter](parameter-object-ado.md) o [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5b08e-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5b08e-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="5b08e-105">Settings and return values</span></span>

<span data-ttu-id="5b08e-106">Establece o devuelve un valor de tipo **Byte** que indica el número de posiciones decimales en las que se resolverán los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="5b08e-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b08e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b08e-107">Remarks</span></span>

<span data-ttu-id="5b08e-108">Utilice la propiedad **NumericScale** para determinar cuántos dígitos a la derecha de la coma decimal se utilizarán para representar valores de un objeto numérico **Parameter** o **Field**.</span><span class="sxs-lookup"><span data-stu-id="5b08e-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="5b08e-109">En los objetos **Parameter**, la propiedad **NumericScale** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5b08e-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="5b08e-p101">En un objeto **Field**, **NumericScale** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **NumericScale** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="5b08e-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

