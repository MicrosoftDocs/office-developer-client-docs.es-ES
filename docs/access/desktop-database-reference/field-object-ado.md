---
title: 'Campo de objeto: objetos de datos ActiveX (ADO)'
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2bf17029a706ad6902a8a01a14e73183f94d7a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715219"
---
# <a name="field-object-ado"></a><span data-ttu-id="c4e4a-102">Field (objeto, ADO)</span><span class="sxs-lookup"><span data-stu-id="c4e4a-102">Field object (ADO)</span></span>


<span data-ttu-id="c4e4a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4e4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4e4a-104">Representa una columna de datos con un tipo de datos común.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e4a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4e4a-105">Remarks</span></span>

<span data-ttu-id="c4e4a-p101">Cada objeto **Field** corresponde a una columna del objeto [Recordset](recordset-object-ado.md). Use la propiedad [Value](value-property-ado.md) de objetos **Field** si desea establecer o devolver datos para el registro actual. Según la funcionalidad expuesta por el proveedor, es posible que algunas colecciones, métodos o propiedades de un objeto **Field** no estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-p101">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md). You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="c4e4a-109">Con las colecciones, los métodos y las propiedades de un objeto **Field**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4e4a-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="c4e4a-110">Devolver el nombre de un campo con la propiedad [Name](name-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4e4a-p102">Ver o cambiar los datos del campo con la propiedad **Value**. **Value** es la propiedad predeterminada del objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-p102">View or change the data in the field with the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="c4e4a-113">Devolver las características básicas de un campo con las propiedades [Tipo](type-property-ado.md), [Precision](precision-property-ado.md) y [NumericScale](numericscale-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="c4e4a-114">Devolver el tamaño declarado de un campo con la propiedad [DefinedSize](definedsize-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4e4a-115">Devolver el tamaño real de los datos de un campo dado con la propiedad [ActualSize](actualsize-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="c4e4a-116">Determinar qué tipos de funcionalidad se admiten para un campo dado con la propiedad [Attributes](attributes-property-ado.md) y la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="c4e4a-117">Manipular los valores de campos que contienen datos de caracteres largos o binarios largos con los métodos [AppendChunk](appendchunk-method-ado.md) y [GetChunk](getchunk-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="c4e4a-118">Si el proveedor admite las actualizaciones por lotes, se pueden resolver las discrepancias de los valores de los campos durante la actualización por lotes con las propiedades [OriginalValue](originalvalue-property-ado.md) y [UnderlyingValue](underlyingvalue-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c4e4a-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="c4e4a-p103">Todas las propiedades de metadatos (**Name**, **Type**, **DefinedSize**, **Precision** y **NumericScale**) están disponibles antes de abrir el objeto **Recordset** del objeto **Field**. Si se establecen en ese momento, se facilita la creación dinámica de formularios.</span><span class="sxs-lookup"><span data-stu-id="c4e4a-p103">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**. Setting them at that time is useful for dynamically constructing forms.</span></span>

