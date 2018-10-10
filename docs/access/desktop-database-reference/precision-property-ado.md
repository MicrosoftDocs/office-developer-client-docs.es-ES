---
title: Precision (propiedad, ADO)
TOCTitle: Precision Property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9e98227e98b4f731cd4d361ff6a2c5394058e86
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486752"
---
# <a name="precision-property-ado"></a><span data-ttu-id="64b75-102">Precision (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="64b75-102">Precision Property (ADO)</span></span>


<span data-ttu-id="64b75-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="64b75-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="64b75-104">Indica el grado de precisión de los valores numéricos de un objeto [Parameter](parameter-object-ado.md) o de los objetos numéricos [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="64b75-104">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="64b75-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="64b75-105">Settings and Return Values</span></span>

<span data-ttu-id="64b75-106">Establece o devuelve un valor de tipo **Byte** que indica el número máximo de dígitos utilizado para representar valores.</span><span class="sxs-lookup"><span data-stu-id="64b75-106">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b75-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64b75-107">Remarks</span></span>

<span data-ttu-id="64b75-108">Utilice la propiedad **Precision** para determinar el número máximo de dígitos utilizado para representar los valores de un objeto numérico **Parameter** o **Field**.</span><span class="sxs-lookup"><span data-stu-id="64b75-108">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="64b75-109">En un objeto **Parameter**, el valor es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="64b75-109">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="64b75-p101">En un objeto **Field**, **Precision** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Precision** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="64b75-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

