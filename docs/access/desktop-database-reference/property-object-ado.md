---
title: Property (objeto, ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b26a305557e2b7244399c6c2c5513909846eaaff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929575"
---
# <a name="property-object-ado"></a>Property (objeto, ADO)


**Se aplica a**: Access 2013, Office 2013

Representa una característica dinámica de un objeto ADO definido por el proveedor.

## <a name="remarks"></a>Comentarios

Los objetos de ADO tienen dos tipos de propiedades: integradas y dinámicas.

Las propiedades integradas son aquellas propiedades implementadas en ADO y disponibles inmediatamente para cualquier objeto nuevo, utilizando la sintaxis. No aparecen como objetos **Property** en la colección [Properties](properties-collection-ado.md) de un objeto, por lo que, aunque se puedan cambiar sus valores, no se pueden modificar sus características.

Las propiedades dinámicas las define el proveedor de datos subyacente y aparecen en la colección **Properties** para el objeto de ADO apropiado. Por ejemplo, una propiedad específica del proveedor puede indicar si un objeto [Recordset](recordset-object-ado.md) admite transacciones o actualizaciones. Estas propiedades adicionales aparecerán como objetos **Property** en la colección **Properties** de ese objeto **Recordset**. Se pueden hacer referencia a las propiedades dinámicas sólo a través de la colección, utilizando el MyObject.Properties(0) u o sintaxis MyObject.Properties.

No se puede eliminar ningún tipo de propiedad.

Un objeto dinámico **Property** tiene cuatro propiedades integradas propias:

  - La propiedad [Name](name-property-ado.md) es una cadena que identifica a la propiedad.

  - La propiedad [Type](type-property-ado.md) es un entero que especifica el tipo de datos de la propiedad.

  - La propiedad [Value](value-property-ado.md) es una variante que contiene la configuración de la propiedad. **Value** es la propiedad predeterminada de un objeto **Property**.

  - La propiedad [Attributes](attributes-property-ado.md) es un valor de tipo Long que indica características de la propiedad específicas del proveedor.

