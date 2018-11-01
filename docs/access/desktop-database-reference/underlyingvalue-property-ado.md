---
title: UnderlyingValue (propiedad, ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d91dccb88ff39ad344ffa0e59e7ccdaaa9f1565
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867786"
---
# <a name="underlyingvalue-property-ado"></a>UnderlyingValue (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013



Indica el valor actual de un objeto [Field](field-object-ado.md) de la base de datos.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant** que indica el valor del objeto **Field**.

## <a name="remarks"></a>Comentarios

Use la propiedad **UnderlyingValue** para devolver el valor actual del campo de la base de datos. El valor del campo de la propiedad **UnderlyingValue** es el valor visible en la transacción y puede ser el resultado de una actualización reciente por parte de otra transacción. Puede diferir de la propiedad [OriginalValue](originalvalue-property-ado.md), que refleja el valor devuelto originalmente al objeto [Recordset](recordset-object-ado.md).

Es similar a utilizar el método [Resync](resync-method-ado.md), aunque la propiedad **UnderlyingValue** sólo devuelve el valor de un campo específico del registro actual. Se trata del mismo valor que el método [Resync](resync-method-ado.md) utiliza para sustituir a la propiedad [Value](value-property-ado.md).

Cuando esta propiedad se utiliza con la propiedad **OriginalValue**, es posible solucionar conflictos que surgen a partir de las actualizaciones por lotes.

## <a name="record"></a>Record

En los objetos [Record](record-object-ado.md), esta propiedad estará vacía para los campos agregados antes de la llamada al método [Update](update-method-ado.md).

