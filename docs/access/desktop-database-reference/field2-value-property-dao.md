---
title: Field2.Value Property (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ae14ee13c0b94a477550b0f20cec2e1fc31fdd6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485224"
---
# <a name="field2value-property-dao"></a>Field2.Value Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve el valor de un objeto. **Variant** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . Valor

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto es un tipo de datos Variant que da como resultado un valor apropiado para el tipo de datos, tal como especifica la propiedad **Type** de un objeto.

En general, la propiedad **Value** se usa para recuperar y alterar los datos en los objetos **Recordset**.

La propiedad **Value** es la propiedad predeterminada de los objetos **Field2**, **Parameter** y **Property**. Por tanto, puede establecer o devolver el valor de uno de esos objetos refiriéndose a ellos directamente en vez de especificar la propiedad **Value**.

Si intenta establecer o devolver la propiedad **Value** en un contexto poco apropiado (por ejemplo, la propiedad **Value** de un objeto **Field2** en la colección **Fields** de un objeto **TableDef**) se producirá un error capturable.


> [!NOTE]
> <P>Cuando se lean valores decimales de una base de datos de Microsoft SQL Server, se les dará formato con notación científica a través de un área de trabajo de Microsoft Access, pero aparecerán como valores decimales normales a través de un área de trabajo de ODBCDirect.</P>


