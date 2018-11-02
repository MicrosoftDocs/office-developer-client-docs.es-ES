---
title: Propiedad Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9aecffc135ab402f02b8fd4e1cc234f4a6eb37d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927329"
---
# <a name="databaseconnection-property-dao"></a>Propiedad Database.Connection (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Conexión

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="remarks"></a>Observaciones

Use la propiedad **Connection** para obtener una referencia a un objeto **Connection** que corresponda al objeto **Database**. En DAO, un objeto **Connection** y su objeto **Database** correspondiente son simplemente dos referencias diferentes de variable de objeto al mismo objeto. La propiedad **[Database](connection-database-property-dao.md)** de un objeto **Connection** y la propiedad **Connection** de un objeto **Database** facilitan el cambio de conexión a un origen de datos ODBC mediante el motor de base de datos de Microsoft Access para utilizar ODBCDirect.

