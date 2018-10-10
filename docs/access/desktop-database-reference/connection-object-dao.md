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
# <a name="connection-object-dao"></a><span data-ttu-id="cf557-102">Connection Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="cf557-102">Connection Object (DAO)</span></span>


<span data-ttu-id="cf557-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf557-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="cf557-p101">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cf557-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>



<span data-ttu-id="cf557-106">Un objeto **Connection** representa una conexión a una base de datos ODBC (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="cf557-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf557-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf557-107">Remarks</span></span>

<span data-ttu-id="cf557-p102">**Connection** es un objeto no persistente que representa una conexión a una base de datos remota. El objeto **Connection** sólo está disponible en áreas de trabajo ODBCDirect (es decir, un objeto **Workspace** creado con la opción de tipo establecida en **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="cf557-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="cf557-p103">[!NOTA] El código escrito para versiones anteriores de DAO puede seguir utilizando el objeto <STRONG>Database</STRONG> por compatibilidad con versiones anteriores, pero si se desea tener las nuevas características de un objeto <STRONG>Connection</STRONG>, debe revisar el código para que utilice el objeto <STRONG>Connection</STRONG>. Para ayudarle con la conversión de código, puede obtener una referencia del objeto <STRONG>Connection</STRONG> desde <STRONG>Database</STRONG> leyendo la propiedad <A href="database-connection-property-dao.md">Connection</A> del objeto <STRONG>Database</STRONG>. A la inversa, puede obtener una referencia del objeto <STRONG>Database</STRONG> desde la propiedad <STRONG>Database</STRONG> del objeto <STRONG>Connection</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="cf557-p103">Code written for earlier versions of DAO can continue to use the <STRONG>Database</STRONG> object for backward compatibility, but if the new features of a <STRONG>Connection</STRONG> are desired, you should revise code to use the <STRONG>Connection</STRONG> object. To help with code conversion, you can obtain a <STRONG>Connection</STRONG> object reference from a <STRONG>Database</STRONG> by reading the <A href="database-connection-property-dao.md">Connection</A> property of the <STRONG>Database</STRONG> object. Conversely, you can obtain a <STRONG>Database</STRONG> object reference from the <STRONG>Connection</STRONG> object's <STRONG>Database</STRONG> property.</span></span></P>


