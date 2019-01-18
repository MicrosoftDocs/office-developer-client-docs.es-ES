---
title: Attributes (propiedad, ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6495c70f64930e1b335c603f13e720ad581203a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717982"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="3911f-102">Attributes (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="3911f-102">Attributes property (ADO)</span></span>


<span data-ttu-id="3911f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3911f-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="3911f-104">Propiedad Attributes</span><span class="sxs-lookup"><span data-stu-id="3911f-104">Attributes Property</span></span>

<span data-ttu-id="3911f-105">Indica una o varias características de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3911f-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3911f-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3911f-106">Settings and return values</span></span>

<span data-ttu-id="3911f-107">Establece o devuelve un valor de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="3911f-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="3911f-p101">Para un objeto [Connection](connection-object-ado.md), la propiedad **Attributes** es de lectura y escritura, y su valor puede ser la suma de uno o varios valores de [XactAttributeEnum](xactattributeenum.md). El valor predeterminado es cero (0).</span><span class="sxs-lookup"><span data-stu-id="3911f-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="3911f-p102">Para un objeto [Parameter](parameter-object-ado.md), la propiedad **Attributes** es de lectura y escritura, y su valor puede ser la suma de uno o varios valores de [ParameterAttributesEnum](parameterattributesenum.md). El valor predeterminado es **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="3911f-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="3911f-p103">Para un objeto [Field](field-object-ado.md), la propiedad **Attributes** puede ser la suma de uno o varios valores de [FieldAttributeEnum](fieldattributeenum.md). Normalmente, es de sólo lectura. Sin embargo, para los objetos **Field** nuevos que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Attributes** es de lectura y escritura sólo después de especificarse la propiedad [Value](value-property-ado.md) del objeto **Field** y de agregar el proveedor correctamente el nuevo objeto **Field** mediante una llamada al método [Update](update-method-ado.md) de la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="3911f-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="3911f-114">Para un objeto [Property](property-object-ado.md), la propiedad **Attributes** es de sólo lectura, y su valor puede ser la suma de uno o varios valores de [PropertyAttributesEnum](propertyattributesenum.md).</span><span class="sxs-lookup"><span data-stu-id="3911f-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3911f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3911f-115">Remarks</span></span>

<span data-ttu-id="3911f-116">Utilice la propiedad **Attributes** para establecer o devolver las características de los objetos **Field**, **Property**, [Connection](field-object-ado.md) o [Parameter](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3911f-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="3911f-p104">Cuando establece varios atributos, puede sumar las constantes apropiadas. Si establece el valor de la propiedad en una suma que incluye constantes incompatibles, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="3911f-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="3911f-119">**Uso de servicio de datos remotos** Esta propiedad no está disponible en un objeto de **conexión** de cliente.</span><span class="sxs-lookup"><span data-stu-id="3911f-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

