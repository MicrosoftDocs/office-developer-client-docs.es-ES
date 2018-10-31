---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a8f324d7216eff2aeeb9045f5c506cdf37170f6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863735"
---
# <a name="connection-object-dao"></a>Connection Object (DAO)


**Se aplica a**: Access 2013 | Office 2013

> [!NOTE]
> [!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.



Un objeto **Connection** representa una conexión a una base de datos ODBC (sólo áreas de trabajo de ODBCDirect).

## <a name="remarks"></a>Observaciones

**Connection** es un objeto no persistente que representa una conexión a una base de datos remota. El objeto **Connection** sólo está disponible en áreas de trabajo ODBCDirect (es decir, un objeto **Workspace** creado con la opción de tipo establecida en **dbUseODBC**).


> [!NOTE]
> [!NOTA] El código escrito para versiones anteriores de DAO puede seguir utilizando el objeto **Database** por compatibilidad con versiones anteriores, pero si se desea tener las nuevas características de un objeto **Connection**, debe revisar el código para que utilice el objeto **Connection**. Para ayudarle con la conversión de código, puede obtener una referencia del objeto **Connection** desde **Database** leyendo la propiedad [Connection](database-connection-property-dao.md) del objeto **Database**. A la inversa, puede obtener una referencia del objeto **Database** desde la propiedad **Database** del objeto **Connection**.


