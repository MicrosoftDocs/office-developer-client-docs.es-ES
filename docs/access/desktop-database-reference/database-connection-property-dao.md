---
title: Database.Connection Property (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d000d2f01bea7746fb249ab7f9acacc047029b21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484425"
---
# <a name="databaseconnection-property-dao"></a>Database.Connection Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Conexión

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="remarks"></a>Observaciones

Use la propiedad **Connection** para obtener una referencia a un objeto **Connection** que corresponda al objeto **Database**. En DAO, un objeto **Connection** y su objeto **Database** correspondiente son simplemente dos referencias diferentes de variable de objeto al mismo objeto. La propiedad **[Database](connection-database-property-dao.md)** de un objeto **Connection** y la propiedad **Connection** de un objeto **Database** facilitan el cambio de conexión a un origen de datos ODBC mediante el motor de base de datos de Microsoft Access para utilizar ODBCDirect.

