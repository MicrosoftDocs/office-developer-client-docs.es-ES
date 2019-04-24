---
title: Objeto Connection (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 73ede9cae5246db3d802125b0f7c4e6df5347930
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295866"
---
# <a name="connection-object-dao"></a><span data-ttu-id="cca6e-102">Objeto Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="cca6e-102">Connection object (DAO)</span></span>

<span data-ttu-id="cca6e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cca6e-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="cca6e-p101">[!NOTA] Las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Utilice ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cca6e-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="cca6e-106">Un objeto **Connection** representa una conexión a una base de datos ODBC (sólo áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="cca6e-106">A **Connection** object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="cca6e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cca6e-107">Remarks</span></span>

<span data-ttu-id="cca6e-p102">**Connection** es un objeto no persistente que representa una conexión a una base de datos remota. El objeto **Connection** sólo está disponible en áreas de trabajo ODBCDirect (es decir, un objeto **Workspace** creado con la opción de tipo establecida en **dbUseODBC**).</span><span class="sxs-lookup"><span data-stu-id="cca6e-p102">A **Connection** is a non-persistent object that represents a connection to a remote database. The **Connection** object is only available in ODBCDirect workspaces (that is, a **Workspace** object created with the type option set to **dbUseODBC**).</span></span>

> [!NOTE]
> <span data-ttu-id="cca6e-p103">[!NOTA] El código escrito para versiones anteriores de DAO puede seguir utilizando el objeto **Database** por compatibilidad con versiones anteriores, pero si se desea tener las nuevas características de un objeto **Connection**, debe revisar el código para que utilice el objeto **Connection**. Para ayudarle con la conversión de código, puede obtener una referencia del objeto **Connection** desde **Database** leyendo la propiedad [Connection](database-connection-property-dao.md) del objeto **Database**. A la inversa, puede obtener una referencia del objeto **Database** desde la propiedad **Database** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="cca6e-p103">Code written for earlier versions of DAO can continue to use the **Database** object for backward compatibility, but if the new features of a **Connection** are desired, you should revise code to use the **Connection** object. To help with code conversion, you can obtain a **Connection** object reference from a **Database** by reading the [Connection](database-connection-property-dao.md) property of the **Database** object. Conversely, you can obtain a **Database** object reference from the **Connection** object's **Database** property.</span></span>


