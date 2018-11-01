---
title: Método Query (RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70f4a1c7a16a97710ef2b0c04bbc0a3924864231
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876032"
---
# <a name="query-method-rds"></a>Query (método, RDS)


**Se aplica a**: Access 2013, Office 2013


Utiliza una cadena de consulta SQL válida para devolver un objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

Establecer el*objeto Recordset* = *DataFactory*. Consulta (*conexión*, *consulta*)

## <a name="parameters"></a>Parámetros

  - *Recordset*

  - Variable de objeto que representa un objeto **Recordset**.

  - *DataFactory*

  - Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).

  - *Connection*

  - Valor de tipo **String** que contiene la información de conexión del servidor. Es similar a la propiedad [Connect](connect-property-rds.md).

  - *Consulta*

  - **String** que contiene la consulta SQL.

## <a name="remarks"></a>Comentarios

La consulta debe utilizar el lenguaje SQL del servidor de base de datos. Se devuelve un estado de resultado si hay un error con la consulta que se ha ejecutado. El método **Query** no comprueba la sintaxis en la cadena de **Query**.

