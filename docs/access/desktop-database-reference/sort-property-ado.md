---
title: Sort (propiedad, ADO)
TOCTitle: Sort Property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e78357e2b662f5b94c2bbcbbe563e4001bcc56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484006"
---
# <a name="sort-property-ado"></a>Sort (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica uno o más nombres de campo por los que se ordena el objeto [Recordset](recordset-object-ado.md), así como si el orden es ascendente o descendente.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String** que indica los nombres de campo del objeto **Recordset** que hay que ordenar. Cada nombre está separado por una coma y va seguido de forma opcional por un espacio en blanco y la palabra clave, **ASC**, que ordena el campo en orden ascendente o **DESC**, que lo hace por orden descendente. De forma predeterminada, si no se especifica palabra clave, el campo se ordena de forma ascendente.

## <a name="remarks"></a>Comentarios

Esta propiedad exige que la propiedad [CursorLocation](cursorlocation-property-ado.md) se establezca en **adUseClient**. Si no existe un índice, se creará uno temporal para cada campo especificado en la propiedad **Sort**.

La operación de ordenación es eficaz debido a que los datos no se reorganizan físicamente, sino que simplemente se obtiene acceso a ellos en el orden especificado por el índice.

Si se establece la propiedad **Sort** en una cadena vacía, se restablecerá el orden original de todas las filas y se eliminarán los índices temporales. Los índices existentes no se eliminarán.

Supongamos que un **objeto Recordset** contiene tres campos denominados *firstName*, *middleInitial*y *LastName (apellidos)*. Establezca la propiedad **Sort** en la cadena "lastName DESC, firstName ASC", que ordenará el **conjunto de registros** por apellidos en orden descendente, a continuación, por nombre en orden ascendente. La inicial media se omite.

Ningún campo puede denominarse "ASC" ni "DESC", ya que esos nombres entran en conflicto con las palabras clave **ASC** y **DESC**. En los campos con nombres en conflicto, utilice un alias mediante la palabra clave **AS** de la consulta que devuelve el objeto **Recordset**.

