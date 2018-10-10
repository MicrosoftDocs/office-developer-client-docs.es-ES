---
title: 'Campo de objeto: objetos de datos ActiveX (ADO)'
TOCTitle: Field Object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 240cb821ec861d33f22d157207cd62a566b4013a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483355"
---
# <a name="field-object-ado"></a>Field (objeto) (ADO)


**Se aplica a**: Access 2013 | Office 2013

Representa una columna de datos con un tipo de datos común.

## <a name="remarks"></a>Comentarios

Cada objeto **Field** corresponde a una columna del objeto [Recordset](recordset-object-ado.md). Use la propiedad [Value](value-property-ado.md) de objetos **Field** si desea establecer o devolver datos para el registro actual. Según la funcionalidad expuesta por el proveedor, es posible que algunas colecciones, métodos o propiedades de un objeto **Field** no estén disponibles.

Con las colecciones, los métodos y las propiedades de un objeto **Field**, puede hacer lo siguiente:

  - Devolver el nombre de un campo con la propiedad [Name](name-property-ado.md).

  - Ver o cambiar los datos del campo con la propiedad **Value**. **Value** es la propiedad predeterminada del objeto **Field**.

  - Devolver las características básicas de un campo con las propiedades [Tipo](type-property-ado.md), [Precision](precision-property-ado.md) y [NumericScale](numericscale-property-ado.md).

  - Devolver el tamaño declarado de un campo con la propiedad [DefinedSize](definedsize-property-ado.md).

  - Devolver el tamaño real de los datos de un campo dado con la propiedad [ActualSize](actualsize-property-ado.md).

  - Determinar qué tipos de funcionalidad se admiten para un campo dado con la propiedad [Attributes](attributes-property-ado.md) y la colección [Properties](properties-collection-ado.md).

  - Manipular los valores de campos que contienen datos de caracteres largos o binarios largos con los métodos [AppendChunk](appendchunk-method-ado.md) y [GetChunk](getchunk-method-ado.md).

  - Si el proveedor admite las actualizaciones por lotes, se pueden resolver las discrepancias de los valores de los campos durante la actualización por lotes con las propiedades [OriginalValue](originalvalue-property-ado.md) y [UnderlyingValue](underlyingvalue-property-ado.md).

Todas las propiedades de metadatos (**Name**, **Type**, **DefinedSize**, **Precision** y **NumericScale**) están disponibles antes de abrir el objeto **Recordset** del objeto **Field**. Si se establecen en ese momento, se facilita la creación dinámica de formularios.

