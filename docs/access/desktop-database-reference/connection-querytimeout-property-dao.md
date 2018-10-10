---
title: Connection.QueryTimeout Property (DAO)
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
ms.openlocfilehash: 51f2f51743a8f92b77fafacebbc18e11eb77fe8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484031"
---
# <a name="connectionquerytimeout-property-dao"></a>Connection.QueryTimeout Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que especifica el número de segundos que hay que esperar antes de que se produzca un error en tiempo de tiempo de espera cuando se ejecuta una consulta en un origen de datos.

## <a name="syntax"></a>Sintaxis

*expresión* . QueryTimeout

*expresión* Variable que representa un objeto **Connection** .

## <a name="remarks"></a>Observaciones

El valor predeterminado es 60.

Cuando esté utilizando una base de datos ODBC como, por ejemplo Microsoft SQL Server, pueden producirse demoras debido al tráfico en la red o a una sobrecarga en el servidor ODBC. En vez de esperar indefinidamente, puede especificar el tiempo de espera.

Cuando use **QueryTimeout** con un objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)**, se especificará un valor global para todas las consultas asociadas con la base de datos. Para invalidar este valor para una consulta específica, establezca la propiedad **ODBCTimeout** del objeto **[QueryDef](querydef-object-dao.md)** particular.

