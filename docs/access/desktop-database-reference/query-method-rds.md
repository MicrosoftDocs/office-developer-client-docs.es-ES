---
title: Método Query (RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a9ecb2d7ebfdd8f6738b8d7b9b8738ce981ec16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483798"
---
# <a name="query-method-rds"></a><span data-ttu-id="a6acc-102">Query (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="a6acc-102">Query Method (RDS)</span></span>


<span data-ttu-id="a6acc-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6acc-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a6acc-104">Utiliza una cadena de consulta SQL válida para devolver un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a6acc-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6acc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6acc-105">Syntax</span></span>

<span data-ttu-id="a6acc-106">Establecer el*objeto Recordset* = *DataFactory*. Consulta (*conexión*, *consulta*)</span><span class="sxs-lookup"><span data-stu-id="a6acc-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="a6acc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6acc-107">Parameters</span></span>

  - <span data-ttu-id="a6acc-108">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="a6acc-108">*Recordset*</span></span>

  - <span data-ttu-id="a6acc-109">Variable de objeto que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a6acc-109">An object variable that represents a **Recordset** object.</span></span>

  - <span data-ttu-id="a6acc-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="a6acc-110">*DataFactory*</span></span>

  - <span data-ttu-id="a6acc-111">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="a6acc-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="a6acc-112">*Connection*</span><span class="sxs-lookup"><span data-stu-id="a6acc-112">*Connection*</span></span>

  - <span data-ttu-id="a6acc-p101">Valor de tipo **String** que contiene la información de conexión del servidor. Es similar a la propiedad [Connect](connect-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="a6acc-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>

  - <span data-ttu-id="a6acc-115">*Consulta*</span><span class="sxs-lookup"><span data-stu-id="a6acc-115">*Query*</span></span>

  - <span data-ttu-id="a6acc-116">**String** que contiene la consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="a6acc-116">A **String** that contains the SQL query.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6acc-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6acc-117">Remarks</span></span>

<span data-ttu-id="a6acc-p102">La consulta debe utilizar el lenguaje SQL del servidor de base de datos. Se devuelve un estado de resultado si hay un error con la consulta que se ha ejecutado. El método **Query** no comprueba la sintaxis en la cadena de **Query**.</span><span class="sxs-lookup"><span data-stu-id="a6acc-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

