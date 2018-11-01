---
title: Recordset2.CacheStart Property (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fb7fd4e2521b8fe712d488f48f2cf6a1b219423
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875892"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="c9b4a-102">Recordset2.CacheStart Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c9b4a-102">Recordset2.CacheStart Property (DAO)</span></span>


<span data-ttu-id="c9b4a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9b4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9b4a-104">Establece o devuelve un valor que especifica el marcador del primer registro de un objeto Recordset de tipo Dynaset que contiene datos que se almacenarán en caché localmente de un origen de datos ODBC (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c9b4a-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b4a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9b4a-105">Syntax</span></span>

<span data-ttu-id="c9b4a-106">*expresión* . CacheStart</span><span class="sxs-lookup"><span data-stu-id="c9b4a-106">*expression* .CacheStart</span></span>

<span data-ttu-id="c9b4a-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="c9b4a-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9b4a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9b4a-108">Remarks</span></span>

<span data-ttu-id="c9b4a-p101">El almacenamiento en la memoria caché de datos mejora el rendimiento si se usan objetos **Recordset** para recuperar datos de un servidor remoto. Una memoria caché es un espacio en la memoria local que contiene los datos recuperados más recientemente en el servidor; esto es útil si los usuarios solicitan los datos de nuevo mientras se ejecuta la aplicación. Cuando los usuarios solicitan datos, el motor de base de datos de Microsoft Access busca primero en la memoria caché los datos solicitados en lugar de recuperarlos del servidor, que requiere más tiempo. En la memoria caché solo se guardan los datos procedentes de un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="c9b4a-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="c9b4a-p102">Un origen de datos ODBC conectado al motor de base de datos de Microsoft Access, por ejemplo una tabla vinculada, puede tener una memoria caché local. Para crear la memoria caché, abra un objeto **Recordset** en el origen de datos remoto, establezca las propiedades **CacheSize** y **[CacheStart](recordset2-cachestart-property-dao.md)**, y use el método **[FillCache](recordset2-fillcache-method-dao.md)** o recorra los registros mediante los métodos **Move**.</span><span class="sxs-lookup"><span data-stu-id="c9b4a-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="c9b4a-p103">El valor de la propiedad **CacheStart** es el marcador del primer registro del objeto **Recordset** que se va a almacenar en la memoria caché. Puede usar el marcador de un registro para establecer la propiedad **CacheStart**. Convierta el registro que desee que comience la memoria caché en el registro actual y establezca la propiedad **CacheStart** con el mismo valor que la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c9b4a-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="c9b4a-118">El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché en la caché y solicita registros fuera del intervalo de caché en el servidor.</span><span class="sxs-lookup"><span data-stu-id="c9b4a-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="c9b4a-119">Los registros recuperados de la caché no reflejan los cambios realizados simultáneamente en el origen de datos por otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="c9b4a-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="c9b4a-120">Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad **CacheSize** del objeto **Recordset** en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, finalmente, use el método **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="c9b4a-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

