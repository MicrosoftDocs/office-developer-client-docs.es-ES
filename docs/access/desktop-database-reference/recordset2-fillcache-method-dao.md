---
title: Método Recordset2. FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2098df82375ac47b7d5abe0bd63b0af2bb29ba40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309705"
---
# <a name="recordset2fillcache-method-dao"></a><span data-ttu-id="f6763-102">Método Recordset2. FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="f6763-102">Recordset2.FillCache method (DAO)</span></span>

<span data-ttu-id="f6763-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6763-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6763-104">Rellena parcial o totalmente una memoria caché local de un objeto **Recordset** que contiene datos de un origen de datos ODBC conectado al motor de base de datos de Microsoft Access (solo bases de datos ODBC conectadas al motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f6763-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6763-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6763-105">Syntax</span></span>

<span data-ttu-id="f6763-106">*expresión* . FillCache (***filas***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="f6763-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="f6763-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="f6763-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6763-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="f6763-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6763-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f6763-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f6763-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="f6763-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f6763-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f6763-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f6763-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6763-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6763-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="f6763-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="f6763-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="f6763-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f6763-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f6763-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f6763-116"><strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica el número de filas que se van a almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="f6763-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="f6763-117">Si se omite este argumento, el valor se determina por el valor de la propiedad <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="f6763-117">If you omit this argument, the value is determined by the <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6763-118"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="f6763-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="f6763-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="f6763-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="f6763-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f6763-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f6763-121"><strong>Variant</strong> (subtipo <strong>String</strong>) que especifica un marcador.</span><span class="sxs-lookup"><span data-stu-id="f6763-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="f6763-122">La caché se rellena empezando por el registro indicado por este marcador.</span><span class="sxs-lookup"><span data-stu-id="f6763-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="f6763-123">Si se omite este argumento, la caché se llena a partir del registro indicado por la propiedad <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="f6763-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f6763-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6763-124">Remarks</span></span>

<span data-ttu-id="f6763-p103">El almacenamiento en caché mejora el rendimiento de una aplicación que recupera datos de un servidor remoto. Una caché es un espacio en una memoria local que conserva los datos recuperados más recientemente del servidor; esto supone que es muy posible que los datos se soliciten de nuevo cuando se ejecute la aplicación. Cuando un usuario solicita datos, el motor de base de datos de Microsoft Access comprueba en la caché los primeros datos en lugar de recuperarlos desde el servidor, lo que tarda más tiempo. La caché no guarda datos que no proceden de un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="f6763-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="f6763-p104">En vez de esperar a que se llene la caché con los registros según se vayan recuperando, puede utilizar el método **FillCache** para llenar de forma explícita la caché en cualquier momento. Esto es más rápido que llenar la caché porque **FillCache** recupera varios registros a la vez en lugar de uno en uno. Por ejemplo, mientras ve cada pantalla de registros, la aplicación utiliza **FillCache** para recuperar la siguiente pantalla de registros que va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="f6763-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="f6763-p105">Cualquier origen de datos ODBC conectado al motor de base de datos de Microsoft Access al que obtenga acceso con objetos **Recordset** puede tener una memoria caché local. Para crear la memoria caché, abra un objeto **Recordset** desde el origen de datos remoto y, a continuación, establezca las propiedades **CacheSize** y **CacheStart** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f6763-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="f6763-134">Si Rows y startbookmark crean un intervalo de registros que se encuentra parcial o totalmente fuera del intervalo de registros especificado por las propiedades **CacheSize** y **CacheStart** , se omite la parte del objeto Recordset fuera de este intervalo y no se cargará. en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="f6763-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="f6763-135">Si **FillCache** solicita más registros que el número restante en el origen de datos remoto, el motor de base de datos de Microsoft Access recupera sólo los registros restantes y no se producen errores.</span><span class="sxs-lookup"><span data-stu-id="f6763-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="f6763-136">Los registros recuperados de la caché no reflejan los cambios concurrentes realizados por otros usuarios en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="f6763-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="f6763-p106">**FillCache** solo recupera los registros que aún no están almacenados en la memoria caché. Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad **CacheSize** del objeto **Recordset** en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, a continuación, use **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="f6763-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="f6763-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6763-139">Example</span></span>

<span data-ttu-id="f6763-p107">En este ejemplo se utilizan los métodos **CreateTableDef** y **FillCache**, y las propiedades **CacheSize**, **CacheStart** y **SourceTableName** para enumerar los registros de una tabla vinculada dos veces. A continuación, se enumeran los registros dos veces con una caché de 50 registros. En este ejemplo se muestran luego las estadísticas de rendimiento para las ejecuciones almacenadas y no almacenadas en caché a través de la tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="f6763-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
       Dim sngStart As Single 
       Dim sngEnd As Single 
       Dim sngNoCache As Single 
       Dim sngCache As Single 
       Dim intLoop As Integer 
       Dim strTemp As String 
       Dim intRecords As Integer 
     
       ' Open a database to which a linked table can be  
       ' appended. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a linked table that connects to a Microsoft SQL 
       ' Server database. 
       Set tdfRoyalties = _ 
          dbsCurrent.CreateTableDef("Royalties") 
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       tdfRoyalties.Connect = _ 
          "ODBC;DATABASE=pubs;DSN=Publishers" 
       tdfRoyalties.SourceTableName = "roysched" 
       dbsCurrent.TableDefs.Append tdfRoyalties 
       Set rstRemote = _ 
          dbsCurrent.OpenRecordset("Royalties") 
     
       With rstRemote 
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          sngStart = Timer 
     
          For intLoop = 1 To 2 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                .MoveNext 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngNoCache = sngEnd - sngStart 
     
          ' Cache the first 50 records. 
          .MoveFirst 
          .CacheSize = 50 
          .FillCache 
          sngStart = Timer 
     
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          For intLoop = 1 To 2 
             intRecords = 0 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                ' Count the records. If the end of the 
                ' cache is reached, reset the cache to the 
                ' next 50 records. 
                intRecords = intRecords + 1 
                .MoveNext 
                If intRecords Mod 50 = 0 Then 
                   .CacheStart = .Bookmark 
                   .FillCache 
                End If 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngCache = sngEnd - sngStart 
     
          ' Display performance results. 
          MsgBox "Caching Performance Results:" & vbCr & _ 
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
