---
title: Propiedad Connection. QueryTimeout (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295824"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="d707e-102">Propiedad Connection. QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="d707e-102">Connection.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="d707e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d707e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d707e-104">Establece o devuelve un valor que especifica el número de segundos que se deben esperar antes de que se produzca un error de tiempo de espera cuando se ejecuta una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="d707e-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="d707e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d707e-105">Syntax</span></span>

<span data-ttu-id="d707e-106">*expresión* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="d707e-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="d707e-107">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="d707e-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d707e-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d707e-108">Remarks</span></span>

<span data-ttu-id="d707e-109">El valor predeterminado es 60.</span><span class="sxs-lookup"><span data-stu-id="d707e-109">The default value is 60.</span></span>

<span data-ttu-id="d707e-p101">Cuando se utiliza una base de datos ODBC, como Microsoft SQL Server, pueden producirse retrasos debido al tráfico de la red o al uso intensivo del servidor ODBC. En lugar de esperar indefinidamente, se puede especificar cuánto tiempo se desea esperar.</span><span class="sxs-lookup"><span data-stu-id="d707e-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="d707e-p102">Cuando use **QueryTimeout** con un objeto **[Connection](connection-object-dao.md)** o **[Database](database-object-dao.md)**, se especificará un valor global para todas las consultas asociadas con la base de datos. Para invalidar este valor para una consulta específica, establezca la propiedad **ODBCTimeout** del objeto **[QueryDef](querydef-object-dao.md)** particular.</span><span class="sxs-lookup"><span data-stu-id="d707e-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

