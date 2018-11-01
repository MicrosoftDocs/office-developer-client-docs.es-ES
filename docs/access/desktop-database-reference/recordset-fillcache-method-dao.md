---
title: Recordset.FillCache Method (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c217fd1cf63477fd8758dfe3d34592fce34cdbca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885216"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="0fd7c-102">Recordset.FillCache Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="0fd7c-102">Recordset.FillCache Method (DAO)</span></span>


<span data-ttu-id="0fd7c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fd7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fd7c-104">Rellena parcial o totalmente una memoria caché local de un objeto **Recordset** que contiene datos de un origen de datos ODBC conectado al motor de base de datos de Microsoft Access (solo bases de datos ODBC conectadas al motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0fd7c-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fd7c-105">Syntax</span></span>

<span data-ttu-id="0fd7c-106">*expresión* . FillCache (***filas***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="0fd7c-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="0fd7c-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0fd7c-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0fd7c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fd7c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0fd7c-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="0fd7c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0fd7c-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="0fd7c-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0fd7c-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0fd7c-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0fd7c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fd7c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fd7c-113">Filas</span><span class="sxs-lookup"><span data-stu-id="0fd7c-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="0fd7c-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="0fd7c-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="0fd7c-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0fd7c-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0fd7c-p101"><strong>Variant</strong> (subtipo <strong>Integer</strong>) que especifica el número de filas que se van a almacenar en caché. Si omite este argumento, el valor se determina mediante el valor de la propiedad <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p101">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache. If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fd7c-118">StartBookmark</span><span class="sxs-lookup"><span data-stu-id="0fd7c-118">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="0fd7c-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="0fd7c-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="0fd7c-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0fd7c-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0fd7c-p102"><strong>Variant</strong> (subtipo <strong>String</strong>) que especifica un marcador. La caché se rellena empezando por el registro indicado por este marcador. Si omite este argumento, la caché se rellena empezando por el registro indicado por la propiedad <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark. The cache is filled starting from the record indicated by this bookmark. If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0fd7c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fd7c-124">Remarks</span></span>

<span data-ttu-id="0fd7c-p103">El almacenamiento en caché mejora el rendimiento de una aplicación que recupera datos de un servidor remoto. Una caché es un espacio en la memoria local que almacena los datos recuperados más recientemente desde el servidor, bajo el supuesto de que los datos se volverán probablemente a recuperar mientras se ejecute la aplicación. Cuando un usuario solicita datos, el motor de base de datos de Microsoft Access comprueba primero los datos en la caché en lugar de recuperarlos del servidor, ya que este proceso tarda más tiempo. La caché no guarda los datos que no proceden de un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="0fd7c-p104">En lugar de esperar a que la caché se rellene con registros conforme éstos se recuperan, puede utilizar el método **FillCache** para rellenar explícitamente la caché en cualquier momento. Éste es un método más rápido para rellenar la caché porque **FillCache** recupera varios registros simultáneamente en lugar de recuperarlos uno por uno. Por ejemplo, mientras ve cada pantalla de registros, la aplicación utiliza **FillCache** para recuperar la siguiente pantalla de registros para su consulta.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="0fd7c-p105">Cualquier origen de datos ODBC conectado al motor de base de datos de Microsoft Access al que obtenga acceso con objetos **Recordset** puede tener una memoria caché local. Para crear la memoria caché, abra un objeto **Recordset** desde el origen de datos remoto y, a continuación, establezca las propiedades **CacheSize** y **CacheStart** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="0fd7c-134">Si rows y startbookmark crean un intervalo de registros que está parcial o totalmente fuera del intervalo de registros especificado por las propiedades **CacheSize** y **CacheStart** , la parte de recordset fuera de este intervalo se omite y no se cargará en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="0fd7c-135">Si **FillCache** solicita más registros que el número restante en el origen de datos remoto, el motor de base de datos de Microsoft Access sólo recupera los registros restantes y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="0fd7c-136">Los registros recuperados de la caché no reflejan los cambios simultáneos realizados por otros usuarios en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span></P>
> <LI>
> <P><span data-ttu-id="0fd7c-p106"><STRONG>FillCache</STRONG> solo recupera los registros que aún no están almacenados en la memoria caché. Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad <STRONG>CacheSize</STRONG> del objeto <STRONG>Recordset</STRONG> en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, a continuación, use <STRONG>FillCache</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p106"><STRONG>FillCache</STRONG> only retrieves records not already cached. To force an update of all the cached data, set the <STRONG>CacheSize</STRONG> property of the <STRONG>Recordset</STRONG> to 0, reset it to the size of the cache you originally requested, and then use <STRONG>FillCache</STRONG>.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="0fd7c-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0fd7c-139">Example</span></span>

<span data-ttu-id="0fd7c-p107">En este ejemplo se utilizan los métodos **CreateTableDef** y **FillCache** y las propiedades **CacheSize**, **CacheStart** y **SourceTableName** para enumerar dos veces los registros de una tabla vinculada. A continuación, se enumeran dos veces los registros con una caché de 50 registros. Por último, se muestran las estadísticas de rendimiento de las ejecuciones con y sin caché a través de la tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="0fd7c-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset 
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
