---
title: NumericScale (propiedad, ADO)
TOCTitle: NumericScale Property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d70144ae886f60285ad22067e0c52b9193a0005
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486304"
---
# <a name="numericscale-property-ado"></a><span data-ttu-id="f2199-102">NumericScale (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="f2199-102">NumericScale Property (ADO)</span></span>


<span data-ttu-id="f2199-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2199-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f2199-104">Indica la escala de valores numéricos de un objeto [Parameter](parameter-object-ado.md) o [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f2199-104">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f2199-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f2199-105">Settings and Return Values</span></span>

<span data-ttu-id="f2199-106">Establece o devuelve un valor de tipo **Byte** que indica el número de posiciones decimales en las que se resolverán los valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="f2199-106">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2199-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2199-107">Remarks</span></span>

<span data-ttu-id="f2199-108">Utilice la propiedad **NumericScale** para determinar cuántos dígitos a la derecha de la coma decimal se utilizarán para representar valores de un objeto numérico **Parameter** o **Field**.</span><span class="sxs-lookup"><span data-stu-id="f2199-108">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="f2199-109">En los objetos **Parameter**, la propiedad **NumericScale** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f2199-109">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="f2199-p101">En un objeto **Field**, **NumericScale** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **NumericScale** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="f2199-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

