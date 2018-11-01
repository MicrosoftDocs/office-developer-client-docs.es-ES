---
title: Size (propiedad, ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03434b0227c5110ac3a1f36512aaaebd5c23c97a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876410"
---
# <a name="size-property-ado"></a>Size (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el tamaño máximo en bytes o caracteres de un objeto [Parameter](parameter-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long** que indica el tamaño máximo en bytes o caracteres de un valor de un objeto **Parameter**.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Size** para determinar el tamaño máximo de los valores que se van a escribir o a leer en la propiedad [Value](value-property-ado.md) de un objeto **Parameter**.

Si se especifica un tipo de datos de longitud variable para un objeto **Parameter** (por ejemplo, cualquiera de tipo **String**, como **adVarChar**), es necesario establecer la propiedad **Size** del objeto antes de anexarlo a la colección [Parameters](parameters-collection-ado.md); de lo contrario, se producirá un error.

Si ya se ha anexado el objeto **Parameter** a la colección **Parameters** de un objeto [Command](command-object-ado.md) y se cambia el tipo de datos por uno de longitud variable, es necesario establecer la propiedad **Size** del objeto **Parameter** antes de ejecutar el objeto **Command**; de lo contrario, se producirá un error.

Si se usa el método [Refresh](refresh-method-ado.md) para obtener información de los parámetros del proveedor y devuelve uno o más objetos **Parameter** de tipo de datos de longitud variable, ADO puede asignar memoria a los parámetros según su tamaño máximo potencial, lo que puede provocar un error durante la ejecución. Para evitar errores, se debe establecer la propiedad **Size** de estos parámetros de forma explícita antes de ejecutar el comando.

La propiedad **Size** es de lectura y escritura.

