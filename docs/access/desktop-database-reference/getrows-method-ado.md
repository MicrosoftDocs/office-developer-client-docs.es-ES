---
title: GetRows (método, ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292226"
---
# <a name="getrows-method-ado"></a>GetRows (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Recupera varios registros de un objeto [Recordset](recordset-object-ado.md) en una matriz.

## <a name="syntax"></a>Sintaxis

** = *conjunto de registros*de matriz. GetRows (*filas*, *Start*, *Fields* )

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant** que es una matriz bidimensional.

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Rows* |Es opcional. Valor de [GetRowsOptionEnum](getrowsoptionenum.md) que indica el número de registros que se van a recuperar. El valor predeterminado es **adGetRowsRest**.|
|*Start* |Es opcional. Valor de tipo **String** o **Variant** que se establece en el marcador del registro donde debe iniciar la operación de **GetRows**. También puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).|
|*Fields* |Es opcional. **Variant** que representa el nombre o la posición ordinal de un solo campo, o bien, una matriz de nombres de campo o números de posición ordinal. ADO devuelve sólo los datos de estos campos.|

## <a name="remarks"></a>Comentarios

Use el método **GetRows** para copiar los registros de un objeto **Recordset** a una matriz bidimensional. El primer subíndice identifica el campo y el segundo identifica el número de registro. La variable de *matriz* se ajusta automáticamente al tamaño correcto cuando el método **GetRows** devuelve los datos.

Si no especifica un valor para el argumento *Rows*, el método **GetRows** recupera automáticamente todos los registros del objeto **Recordset**. Si solicita más registros de los que están disponibles, **GetRows** devuelve sólo el número de registros disponibles.

Si el objeto **Recordset** admite marcadores, puede especificar en qué registro el método **GetRows** debe comenzar a recuperar datos pasando el valor de la propiedad [Bookmark](bookmark-property-ado.md) de ese registro en el argumento *Start*.

Si desea restringir los campos que debe devolver la llamada a **GetRows**, puede pasar el número o el nombre de un solo campo, o bien, una matriz de números y nombres de campo en el argumento *Fields*.

Tras llamar a **GetRows**, el siguiente registro sin leer se convierte en el registro actual, o bien, el valor de la propiedad [EOF](bof-eof-properties-ado.md) se establece en **True** si no quedan registros.

