---
title: Propiedad Property.Value (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e7c79fe12b3b7bfe98e0c7547f4ed2d12b148ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301172"
---
# <a name="propertyvalue-property-dao"></a>Propiedad Property.Value (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el valor de un objeto. **Variant** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . Valor

*expresión* Variable que representa un **objeto Property.**

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un tipo de datos Variant que evalúa en un valor apropiado para el tipo de datos, como el especificado por la propiedad de un objeto **Type**.

En general, la propiedad **Value** se usa para recuperar y alterar los datos en los objetos **Recordset**.

La propiedad **Value** es la propiedad predeterminada de los objetos **Field**, **Parameter** y **Property**. Por tanto, puede establecer o devolver el valor de uno de esos objetos al referirse a ellos directamente en vez de especificar la propiedad **Value**.

Si intenta establecer o devolver la propiedad **Value** en un contexto poco apropiado (por ejemplo, la propiedad **Value** de un objeto **Field** en la colección **Fields** de un objeto **TableDef**) se producirá un error capturable.

> [!NOTE]
> Cuando se lean valores decimales de una base de datos de Microsoft SQL Server, se les dará formato con notación científica a través de un área de trabajo de Microsoft Access, pero aparecerán como valores decimales normales a través de un área de trabajo de ODBCDirect.


