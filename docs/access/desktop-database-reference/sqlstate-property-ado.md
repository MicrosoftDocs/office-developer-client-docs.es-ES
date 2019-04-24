---
title: SQLState (propiedad, ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb4a9adbc6060b7c33e128a0a3fca8c1eb7bc10d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308557"
---
# <a name="sqlstate-property-ado"></a>SQLState (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el estado SQL de un objeto [Error](error-object-ado.md) especificado.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de cinco caracteres de tipo **String** que sigue el estándar ANSI SQL e indica el código del error.

## <a name="remarks"></a>Comentarios

Use la propiedad **SQLState** para leer el código de error de cinco caracteres que devuelve el proveedor cuando se produce un error durante el procesamiento de una instrucción SQL. Por ejemplo, cuando se usa el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error de estado SQL se originan en ODBC, basándose en errores específicos de ODBC o en errores que se originan en Microsoft SQL Server, y se asignan a errores ODBC. Estos códigos de error están documentados en el estándar ANSI de SQL, pero pueden ser implementados de formas diferentes por los distintos orígenes de datos.

