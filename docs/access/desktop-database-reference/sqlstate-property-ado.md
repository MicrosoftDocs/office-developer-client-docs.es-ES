---
title: SQLState (propiedad, ADO)
TOCTitle: SQLState Property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aead95e4276d61d69ae6ba5a86974cbe630f9043
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484989"
---
# <a name="sqlstate-property-ado"></a>SQLState (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el estado SQL de un objeto [Error](error-object-ado.md) especificado.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de cinco caracteres de tipo **String** que sigue el estándar ANSI SQL e indica el código del error.

## <a name="remarks"></a>Comentarios

Use la propiedad **SQLState** para leer el código de error de cinco caracteres que devuelve el proveedor cuando se produce un error durante el procesamiento de una instrucción SQL. Por ejemplo, cuando se usa el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error de estado SQL se originan en ODBC, basándose en errores específicos de ODBC o en errores que se originan en Microsoft SQL Server, y se asignan a errores ODBC. Estos códigos de error están documentados en el estándar ANSI de SQL, pero pueden ser implementados de formas diferentes por los distintos orígenes de datos.

