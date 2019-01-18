---
title: Propiedad Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77d9bfa30dbfab21fd75de36b336a25e6af3187e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709841"
---
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="24da2-102">Propiedad Database.Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="24da2-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="24da2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24da2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="24da2-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24da2-104">Syntax</span></span>

<span data-ttu-id="24da2-105">*expresión* . Conexión</span><span class="sxs-lookup"><span data-stu-id="24da2-105">*expression* .Connection</span></span>

<span data-ttu-id="24da2-106">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="24da2-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="24da2-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24da2-107">Remarks</span></span>

<span data-ttu-id="24da2-p101">Use la propiedad **Connection** para obtener una referencia a un objeto **Connection** que corresponda al objeto **Database**. En DAO, un objeto **Connection** y su objeto **Database** correspondiente son simplemente dos referencias diferentes de variable de objeto al mismo objeto. La propiedad **[Database](connection-database-property-dao.md)** de un objeto **Connection** y la propiedad **Connection** de un objeto **Database** facilitan el cambio de conexión a un origen de datos ODBC mediante el motor de base de datos de Microsoft Access para utilizar ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="24da2-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

