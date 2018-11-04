---
title: Método Query (RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e7f9dfc3ce5cb0d757951f13c1078ab44d04760
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949428"
---
# <a name="query-method-rds"></a><span data-ttu-id="72b18-102">Query (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="72b18-102">Query method (RDS)</span></span>

<span data-ttu-id="72b18-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72b18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72b18-104">Utiliza una cadena de consulta SQL válida para devolver un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72b18-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="72b18-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72b18-105">Syntax</span></span>

<span data-ttu-id="72b18-106">Establecer el*objeto Recordset* = *DataFactory*. Consulta (*conexión*, *consulta*)</span><span class="sxs-lookup"><span data-stu-id="72b18-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="72b18-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72b18-107">Parameters</span></span>

|<span data-ttu-id="72b18-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="72b18-108">Parameter</span></span>|<span data-ttu-id="72b18-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="72b18-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="72b18-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="72b18-110">*Recordset*</span></span> |<span data-ttu-id="72b18-111">Variable de objeto que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="72b18-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="72b18-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="72b18-112">*DataFactory*</span></span> |<span data-ttu-id="72b18-113">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="72b18-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="72b18-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="72b18-114">*Connection*</span></span> |<span data-ttu-id="72b18-p101">Valor de tipo **String** que contiene la información de conexión del servidor. Es similar a la propiedad [Connect](connect-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="72b18-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="72b18-117">*Consulta*</span><span class="sxs-lookup"><span data-stu-id="72b18-117">*Query*</span></span> |<span data-ttu-id="72b18-118">**String** que contiene la consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="72b18-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="72b18-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72b18-119">Remarks</span></span>

<span data-ttu-id="72b18-p102">La consulta debe utilizar el lenguaje SQL del servidor de base de datos. Se devuelve un estado de resultado si hay un error con la consulta que se ha ejecutado. El método **Query** no comprueba la sintaxis en la cadena de **Query**.</span><span class="sxs-lookup"><span data-stu-id="72b18-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

