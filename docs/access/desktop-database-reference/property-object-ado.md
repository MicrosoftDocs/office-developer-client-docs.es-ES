---
title: Objeto Property (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302922"
---
# <a name="property-object-ado"></a>Objeto Property (ADO)


**Se aplica a:** Access 2013, Office 2013

Representa una característica dinámica de un objeto ADO definido por el proveedor.

## <a name="remarks"></a>Comentarios

Los objetos de ADO tienen dos tipos de propiedades: integradas y dinámicas.

Las propiedades integradas son aquellas propiedades implementadas en ADO y disponibles inmediatamente para cualquier objeto nuevo, mediante la sintaxis. No aparecen como objetos **Property** en la colección [Properties](properties-collection-ado.md) de un objeto, por lo que, aunque se puedan cambiar sus valores, no se pueden modificar sus características.

Las propiedades dinámicas las define el proveedor de datos subyacente y aparecen en la colección **Properties** para el objeto de ADO apropiado. Por ejemplo, una propiedad específica del proveedor puede indicar si un objeto [Recordset](recordset-object-ado.md) admite transacciones o actualizaciones. Estas propiedades adicionales aparecerán como objetos **Property** en la colección **Properties** de ese objeto **Recordset**. Sólo se puede hacer referencia a las propiedades dinámicas a través de la colección, mediante la sintaxis MyObject.Properties(0) o MyObject.Properties("Name").

No se puede eliminar ningún tipo de propiedad.

Un objeto dinámico **Property** tiene cuatro propiedades integradas propias:

  - La propiedad [Name](name-property-ado.md) es una cadena que identifica la propiedad.

  - La propiedad [Type](type-property-ado.md) es un entero que especifica el tipo de datos de la propiedad.

  - La propiedad [Value](value-property-ado.md) es una variante que contiene la configuración de la propiedad. **Value** es la propiedad predeterminada de un objeto **Property**.

  - La propiedad [Attributes](attributes-property-ado.md) es un valor de tipo Long que indica características de la propiedad específicas del proveedor.

