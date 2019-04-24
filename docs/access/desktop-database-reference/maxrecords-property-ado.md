---
title: MaxRecords (propiedad, ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289724"
---
# <a name="maxrecords-property-ado"></a>MaxRecords (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el número máximo de registros que se va a devolver a un objeto [Recordset](recordset-object-ado.md) desde una consulta.

## <a name="settings-and-return-values"></a>Valores de configuración y devueltos

Establece o devuelve un valor de tipo **Long** que indica el número máximo de registros que se va a devolver. El valor predeterminado es cero (sin límite).

## <a name="remarks"></a>Comentarios

Use la propiedad **MaxRecords** para limitar el número de registros que devuelve el proveedor desde el origen de datos. El valor predeterminado de esta propiedad es cero, lo que significa que el proveedor devuelve todos los registros solicitados.

La propiedad **MaxRecords** es de lectura y escritura cuando el objeto **Recordset** está cerrado, y es de solo lectura cuando está abierto.

