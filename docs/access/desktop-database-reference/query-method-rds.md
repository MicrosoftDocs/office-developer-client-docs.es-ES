---
title: Método Query (referencia de base de datos de escritorio de Access de RDS)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301116"
---
# <a name="query-method-rds"></a>Query (método, RDS)

**Se aplica a:** Access 2013, Office 2013

Utiliza una cadena de consulta SQL válida para devolver un objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

Establezca el valor de*DataFactory*del*objeto Recordset* = . Consulta (*conexión*, *consulta*)

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Recordset* |Variable de objeto que representa un objeto **Recordset**.|
|*DataFactory* |Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connection* |Valor de tipo **String** que contiene la información de conexión del servidor. Es similar a la propiedad [Connect](connect-property-rds.md).|
|*Consulta* |**String** que contiene la consulta SQL.|

## <a name="remarks"></a>Comentarios

La consulta debe utilizar el lenguaje SQL del servidor de base de datos. Se devuelve un estado de resultado si hay un error con la consulta que se ha ejecutado. El método **Query** no comprueba la sintaxis en la cadena de **Query**.

