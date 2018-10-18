---
title: GetRows (método, ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0f7f38e44e26238e5a55feaaad302bbf427d678
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606153"
---
# <a name="getrows-method-ado"></a>GetRows (método, ADO)


**Se aplica a**: Access 2013 | Office 2013


Recupera varios registros de un objeto [Recordset](recordset-object-ado.md) en una matriz.

## <a name="syntax"></a>Sintaxis

*matriz* = *conjunto de registros*. GetRows (*filas*, *Iniciar*, *campos* )

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Devuelve un valor de tipo **Variant** que es una matriz bidimensional.

## <a name="parameters"></a>Parámetros

  - *Rows*

  - Es opcional. Valor de [GetRowsOptionEnum](getrowsoptionenum.md) que indica el número de registros que se van a recuperar. El valor predeterminado es **adGetRowsRest**.

  - *Start*

  - Es opcional. Valor de tipo **String** o **Variant** que se establece en el marcador del registro donde debe iniciar la operación de **GetRows**. También puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).

  - *Fields*

  - Es opcional. **Variant** que representa el nombre o la posición ordinal de un solo campo, o bien, una matriz de nombres de campo o números de posición ordinal. ADO devuelve sólo los datos de estos campos.

## <a name="remarks"></a>Comentarios

Use el método **GetRows** para copiar los registros de un objeto **Recordset** a una matriz bidimensional. El primer subíndice identifica el campo y el segundo identifica el número de registro. La variable de *matriz* se ajusta automáticamente al tamaño correcto cuando el método **GetRows** devuelve los datos.

Si no especifica un valor para el argumento *Rows* , el método **GetRows** recupera automáticamente todos los registros en el objeto **Recordset** . Si solicita más registros de los que están disponibles, **GetRows** devuelve sólo el número de registros disponibles.

Si el objeto **Recordset** admite marcadores, puede especificar en qué registro el método **GetRows** debe comenzar a recuperar datos pasando el valor de propiedad de [Bookmark](bookmark-property-ado.md) de ese registro en el argumento *Start* .

Si desea restringir los campos que devuelve la llamada a **GetRows** , puede pasar un nombre o número del campo único o una matriz de números y nombres de campo en el argumento *Fields* .

Tras llamar a **GetRows**, el siguiente registro sin leer se convierte en el registro actual, o bien, el valor de la propiedad [EOF](bof-eof-properties-ado.md) se establece en **True** si no quedan registros.

