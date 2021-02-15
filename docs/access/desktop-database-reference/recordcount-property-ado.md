---
title: Propiedad RecordCount (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300773"
---
# <a name="recordcount-property-ado"></a>Propiedad RecordCount (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el número de registros de un objeto [Recordset](recordset-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que indica el número de registros del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Use la propiedad **RecordCount** para descubrir cuántos registros hay en un objeto **Recordset**. La propiedad devuelve -1 cuando ADO no puede determinar el número de registros o si el proveedor o el tipo de cursor no admite la propiedad **RecordCount**. Al leer la propiedad **RecordCount** en un objeto **Recordset** cerrado se produce un error.

Si el objeto **Recordset** es compatible con un posicionamiento aproximado o con marcadores, es decir, **Supports (adApproxPosition)** o **Supports (adBookmark)** devuelven respectivamente **True**, este valor será el número exacto de registros en el objeto **Recordset**, independientemente de si se ha rellenado por completo. Si el objeto **Recordset** no es compatible con un posicionamiento aproximado, esta propiedad puede suponer una considerable pérdida de recursos, dado que será necesario recuperar y contar todos los registros para devolver un valor de **RecordCount** preciso.

El tipo de cursor del objeto **Recordset** afecta a la posibilidad de determinar el número de registros. La propiedad **RecordCount** devolverá -1 para un cursor de sólo avance, el recuento real para un cursor estático o de conjunto de claves y -1 o el recuento real para un cursor dinámico, según el origen de datos.

