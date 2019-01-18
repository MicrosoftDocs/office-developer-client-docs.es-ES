---
title: Type (propiedad, ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698256"
---
# <a name="type-property-ado"></a>Type (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el tipo operativo o tipo de datos de un objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) o [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Comentarios

En objetos **Parameter**, la propiedad **Type** es de lectura y escritura. En los nuevos objetos **Field** que se han anexado a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Type** sólo es de lectura y escritura después de que se haya especificado la propiedad [Value](value-property-ado.md) del objeto **Field** y el proveedor de datos haya agregado correctamente el nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.

En el resto de los objetos, la propiedad **Type** es de sólo lectura.

