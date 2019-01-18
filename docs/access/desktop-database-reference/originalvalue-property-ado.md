---
title: OriginalValue (propiedad, ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700426"
---
# <a name="originalvalue-property-ado"></a>OriginalValue (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica el valor de un objeto [Field](field-object-ado.md) que existía en el registro antes de la realización de cualquier cambio.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant** que representa el valor de un campo antes de la realización de cualquier cambio.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **OriginalValue** para devolver el valor original de campo de un campo del registro actual.

En el *modo de actualización inmediata* (en la que el proveedor escribe los cambios en el origen de datos subyacente después de llamar al método [Update](update-method-ado.md) ), la propiedad **OriginalValue** devuelve el valor de campo que existía antes de cualquier cambio (es decir, desde el última llamada al método **Update** ). Es el mismo valor que usa el método [CancelUpdate](cancelupdate-method-ado.md) para sustituir a la propiedad [Value](value-property-ado.md).

En *el modo de actualización por lotes* (en el que el proveedor almacena varios cambios en caché y los escribe en el origen de datos subyacente sólo cuando se llama al método [UpdateBatch](updatebatch-method-ado.md) ), la propiedad **OriginalValue** devuelve el valor de campo que existía antes de cualquier los cambios (es decir, desde el último método **UpdateBatch** (llamada). Es el mismo valor que utiliza el método [CancelBatch](cancelbatch-method-ado.md) para sustituir a la propiedad **Value**. Cuando se utiliza esta propiedad con la propiedad [UnderlyingValue](underlyingvalue-property-ado.md), es posible solucionar conflictos que surgen a partir de las actualizaciones por lotes.

## <a name="record"></a>Record

En los objetos [Record](record-object-ado.md), la propiedad **OriginalValue** estará vacía para los campos agregados antes de la llamada al método [Update](update-method-ado.md).

