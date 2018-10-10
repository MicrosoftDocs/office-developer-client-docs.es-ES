---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484131"
---
# <a name="connection-object-dao"></a>Connection Object (DAO)


**Se aplica a**: Access 2013 | Office 2013


> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>



Un objeto **Connection** representa una conexión a una base de datos ODBC (sólo áreas de trabajo de ODBCDirect).

## <a name="remarks"></a>Observaciones

**Connection** es un objeto no persistente que representa una conexión a una base de datos remota. El objeto **Connection** sólo está disponible en áreas de trabajo ODBCDirect (es decir, un objeto **Workspace** creado con la opción de tipo establecida en **dbUseODBC**).


> [!NOTE]
> <P>[!NOTA] El código escrito para versiones anteriores de DAO puede seguir utilizando el objeto <STRONG>Database</STRONG> por compatibilidad con versiones anteriores, pero si se desea tener las nuevas características de un objeto <STRONG>Connection</STRONG>, debe revisar el código para que utilice el objeto <STRONG>Connection</STRONG>. Para ayudarle con la conversión de código, puede obtener una referencia del objeto <STRONG>Connection</STRONG> desde <STRONG>Database</STRONG> leyendo la propiedad <A href="database-connection-property-dao.md">Connection</A> del objeto <STRONG>Database</STRONG>. A la inversa, puede obtener una referencia del objeto <STRONG>Database</STRONG> desde la propiedad <STRONG>Database</STRONG> del objeto <STRONG>Connection</STRONG>.</P>


