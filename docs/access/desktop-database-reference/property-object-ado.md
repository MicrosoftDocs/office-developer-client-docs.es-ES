---
title: Property (objeto) (ADO)
TOCTitle: Property Object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b3cb4d5caedb6e73bf0819639c1feac12b9d3a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483745"
---
# <a name="property-object-ado"></a><span data-ttu-id="3d269-102">Property (objeto) (ADO)</span><span class="sxs-lookup"><span data-stu-id="3d269-102">Property Object (ADO)</span></span>


<span data-ttu-id="3d269-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d269-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d269-104">Representa una característica dinámica de un objeto ADO definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3d269-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d269-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d269-105">Remarks</span></span>

<span data-ttu-id="3d269-106">Los objetos de ADO tienen dos tipos de propiedades: integradas y dinámicas.</span><span class="sxs-lookup"><span data-stu-id="3d269-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="3d269-107">Las propiedades integradas son aquellas propiedades implementadas en ADO y disponibles inmediatamente para cualquier objeto nuevo, utilizando la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="3d269-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="3d269-108">No aparecen como objetos **Property** en la colección [Properties](properties-collection-ado.md) de un objeto, por lo que, aunque se puedan cambiar sus valores, no se pueden modificar sus características.</span><span class="sxs-lookup"><span data-stu-id="3d269-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="3d269-109">Las propiedades dinámicas las define el proveedor de datos subyacente y aparecen en la colección **Properties** para el objeto de ADO apropiado.</span><span class="sxs-lookup"><span data-stu-id="3d269-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="3d269-110">Por ejemplo, una propiedad específica del proveedor puede indicar si un objeto [Recordset](recordset-object-ado.md) admite transacciones o actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="3d269-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="3d269-111">Estas propiedades adicionales aparecerán como objetos **Property** en la colección **Properties** de ese objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3d269-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="3d269-112">Se pueden hacer referencia a las propiedades dinámicas sólo a través de la colección, utilizando el MyObject.Properties(0) u o sintaxis MyObject.Properties.</span><span class="sxs-lookup"><span data-stu-id="3d269-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="3d269-113">No se puede eliminar ningún tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3d269-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="3d269-114">Un objeto dinámico **Property** tiene cuatro propiedades integradas propias:</span><span class="sxs-lookup"><span data-stu-id="3d269-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="3d269-115">La propiedad [Name](name-property-ado.md) es una cadena que identifica a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3d269-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="3d269-116">La propiedad [Type](type-property-ado.md) es un entero que especifica el tipo de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3d269-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="3d269-p103">La propiedad [Value](value-property-ado.md) es una variante que contiene la configuración de la propiedad. **Value** es la propiedad predeterminada de un objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="3d269-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="3d269-119">La propiedad [Attributes](attributes-property-ado.md) es un valor de tipo Long que indica características de la propiedad específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3d269-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>
