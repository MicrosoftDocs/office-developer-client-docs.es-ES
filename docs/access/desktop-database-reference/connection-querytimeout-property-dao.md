---
title: Propiedad Connection.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711094"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="085c2-102">Propiedad Connection.QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="085c2-102">Connection.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="085c2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="085c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="085c2-104">Establece o devuelve un valor que especifica el número de segundos que hay que esperar antes de que se produzca un error en tiempo de tiempo de espera cuando se ejecuta una consulta en un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="085c2-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="085c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="085c2-105">Syntax</span></span>

<span data-ttu-id="085c2-106">*expresión* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="085c2-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="085c2-107">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="085c2-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="085c2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="085c2-108">Remarks</span></span>

<span data-ttu-id="085c2-109">El valor predeterminado es 60.</span><span class="sxs-lookup"><span data-stu-id="085c2-109">The default value is 60.</span></span>

<span data-ttu-id="085c2-p101">Cuando esté utilizando una base de datos ODBC como, por ejemplo Microsoft SQL Server, pueden producirse demoras debido al tráfico en la red o a una sobrecarga en el servidor ODBC. En vez de esperar indefinidamente, puede especificar el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="085c2-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="085c2-p102">Cuando use **QueryTimeout** con un objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)**, se especificará un valor global para todas las consultas asociadas con la base de datos. Para invalidar este valor para una consulta específica, establezca la propiedad **ODBCTimeout** del objeto **[QueryDef](querydef-object-dao.md)** particular.</span><span class="sxs-lookup"><span data-stu-id="085c2-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

