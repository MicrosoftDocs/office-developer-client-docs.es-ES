---
title: Database.Connection Property (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0974051b1f10fa73caad6d9feafb2e2b769579
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882843"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="dae22-102">Database.Connection Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="dae22-102">Database.Connection Property (DAO)</span></span>


<span data-ttu-id="dae22-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dae22-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="dae22-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dae22-104">Syntax</span></span>

<span data-ttu-id="dae22-105">*expresión* . Conexión</span><span class="sxs-lookup"><span data-stu-id="dae22-105">*expression* .Connection</span></span>

<span data-ttu-id="dae22-106">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="dae22-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae22-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dae22-107">Remarks</span></span>

<span data-ttu-id="dae22-p101">Use la propiedad **Connection** para obtener una referencia a un objeto **Connection** que corresponda al objeto **Database**. En DAO, un objeto **Connection** y su objeto **Database** correspondiente son simplemente dos referencias diferentes de variable de objeto al mismo objeto. La propiedad **[Database](connection-database-property-dao.md)** de un objeto **Connection** y la propiedad **Connection** de un objeto **Database** facilitan el cambio de conexión a un origen de datos ODBC mediante el motor de base de datos de Microsoft Access para utilizar ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="dae22-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

