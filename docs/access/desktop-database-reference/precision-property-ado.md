---
title: Propiedad Precision (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 662e5e9287da1ccfb81c727f5d5e5dfedce2969b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287478"
---
# <a name="precision-property-ado"></a>Propiedad Precision (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el grado de precisión de los valores numéricos de un objeto [Parameter](parameter-object-ado.md) o de los objetos numéricos [Field](field-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Byte** que indica el número máximo de dígitos utilizado para representar valores.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Precision** para determinar el número máximo de dígitos utilizado para representar los valores de un objeto numérico **Parameter** o **Field**.

En un objeto **Parameter**, el valor es de lectura y escritura.

En un objeto **Field**, **Precision** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Precision** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.

