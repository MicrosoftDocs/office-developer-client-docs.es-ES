---
title: RecordCount (propiedad, ADO)
TOCTitle: RecordCount Property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a619570264973fc70b7cc5bd581437a4002b00be
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486164"
---
# <a name="recordcount-property-ado"></a>RecordCount (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el número de registros de un objeto [Recordset](recordset-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que indica el número de registros del objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Use la propiedad **RecordCount** para descubrir cuántos registros hay en un objeto **Recordset**. La propiedad devuelve -1 cuando ADO no puede determinar el número de registros o si el proveedor o el tipo de cursor no admite la propiedad **RecordCount**. Al leer la propiedad **RecordCount** en un objeto **Recordset** cerrado se produce un error.

Si el objeto **Recordset** es compatible con un posicionamiento aproximado o con marcadores, es decir, **Supports (adApproxPosition)** o **Supports (adBookmark)** devuelven respectivamente **True**, este valor será el número exacto de registros en el objeto **Recordset**, independientemente de si se ha rellenado por completo. Si el objeto **Recordset** no es compatible con un posicionamiento aproximado, esta propiedad puede suponer una considerable pérdida de recursos, dado que será necesario recuperar y contar todos los registros para devolver un valor de **RecordCount** preciso.

El tipo de cursor del objeto **Recordset** afecta a la posibilidad de determinar el número de registros. La propiedad **RecordCount** devolverá -1 para un cursor de sólo avance, el recuento real para un cursor estático o de conjunto de claves y -1 o el recuento real para un cursor dinámico, según el origen de datos.

