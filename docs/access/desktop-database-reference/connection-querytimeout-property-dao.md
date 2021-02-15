---
title: Propiedad Connection.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295824"
---
# <a name="connectionquerytimeout-property-dao"></a>Propiedad Connection.QueryTimeout (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que especifica el número de segundos que se deben esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta una consulta en un origen de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . QueryTimeout

*expression* Variable que representa un objeto **Connection**.

## <a name="remarks"></a>Comentarios

El valor predeterminado es 60.

Cuando se utiliza una base de datos ODBC, como Microsoft SQL Server, pueden producirse retrasos debido al tráfico de la red o al uso intensivo del servidor ODBC. En lugar de esperar indefinidamente, se puede especificar cuánto tiempo se desea esperar.

Cuando use **QueryTimeout** con un objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)**, se especificará un valor global para todas las consultas asociadas con la base de datos. Para invalidar este valor para una consulta específica, establezca la propiedad **ODBCTimeout** del objeto **[QueryDef](querydef-object-dao.md)** particular.

