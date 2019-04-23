---
title: Constantes enumeradas de ADO
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283411"
---
# <a name="ado-enumerated-constants"></a><span data-ttu-id="2d8b0-102">Constantes enumeradas de ADO</span><span class="sxs-lookup"><span data-stu-id="2d8b0-102">ADO enumerated constants</span></span>

<span data-ttu-id="2d8b0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d8b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d8b0-p101">Para ayudar en la depuración, las enumeraciones ADO muestran un valor para cada constante. Sin embargo, este valor es puramente consultivo y puede cambiar de una versión a otra de ADO. El código sólo debería depender del nombre, no del valor real, de cada constante enumerada.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="2d8b0-107">Constante enumerada</span><span class="sxs-lookup"><span data-stu-id="2d8b0-107">Enumerated constant</span></span></th>
<th><span data-ttu-id="2d8b0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d8b0-108">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-109"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-110">Para un objeto <strong>Recordset</strong> RDS, especifica la prioridad de ejecución del subproceso asincrónico que recupera datos.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-110">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-111"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-112">Especifica cuándo el proveedor <strong>MSDataShape</strong> vuelve a calcular columnas agregadas y calculadas en un objeto <strong>Recordset</strong> jerárquico.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-112">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-113"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-114">Especifica qué campos se pueden usar para detectar conflictos durante una actualización optimista de una fila del origen de datos con un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-114">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-115"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-116">Especifica si el método <strong>UpdateBatch</strong> va seguido de una operación implícita del método <strong>Resync</strong> y, en ese caso, el ámbito de esa operación.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-116">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-117"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-117"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-118">Especifica a qué registros afecta una operación.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-118">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-119"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-119"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-120">Especifica un marcador que indica dónde debe comenzar la operación.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-120">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-121"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-122">Especifica cómo se debe interpretar un argumento de comando.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-122">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-123"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-123"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-124">Especifica la posición relativa de dos registros representados por sus marcadores.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-124">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-125"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-126">Especifica los permisos disponibles para modificar datos de un objeto <strong>Connection</strong>, abrir un <strong>Record</strong> o especificar valores para la propiedad <strong>Mode</strong> de los objetos <strong>Record</strong> y <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-126">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-127"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-128">Especifica si el método <strong>Open</strong> de un objeto <strong>Connection</strong> debe volver después (sincrónicamente) o antes (asincrónicamente) de que la conexión se establezca.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-128">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-129"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-130">Especifica si se debe mostrar un cuadro de diálogo para pedir parámetros que faltan al abrir una conexión con un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-130">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-131"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-132">Especifica el comportamiento del método <strong>CopyRecord</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-132">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-133"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-134">Especifica la ubicación del motor de cursor.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-134">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-135"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-136">Especifica qué funcionalidad debería probar el método <strong>Supports</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-136">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-137"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-138">Especifica el tipo de cursor usado en un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-138">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-139"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-139"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-140">Especifica el tipo de datos de un <strong>campo</strong>, <strong>parámetro</strong> o <strong>propiedad</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-140">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-141"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-141"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-142">Especifica el estado de edición de un registro.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-142">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-143"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-144">Especifica el tipo de error ADO en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-144">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-145"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-145"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-146">Especifica el motivo que ocasionó un evento.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-146">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-147"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-147"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-148">Especifica el estado actual de la ejecución de un evento.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-148">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-149"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-150">Especifica la forma en que un proveedor debe ejecutar un comando.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-150">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-151"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-151"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-152">Especifica los campos especiales a los que se hace referencia en la colección <strong>Fields</strong> de un objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-152">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-153"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-154">Especifica uno o más atributos de un objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-154">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-155"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-156">Especifica el estado de un objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-156">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-157"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-158">Especifica el grupo de registros que se deben filtrar en un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-158">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-159"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-160">Especifica cuántos registros se deben recuperar de un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-160">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-161"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-162">Especifica el nivel de aislamiento de transacción para un objeto <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-162">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-163"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-164">Especifica el carácter utilizado como separador de línea en objetos <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-164">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-165"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-165"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-166">Especifica el tipo de bloqueo colocado en registros durante su modificación.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-166">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-167"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-168">Especifica qué registros se deben devolver al servidor.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-168">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-169"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-170">Especifica el comportamiento del método <strong>MoveRecord</strong> del objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-170">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-171"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-171"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-172">Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-172">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-173"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-174">Especifica los atributos de un objeto <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-174">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-175"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-176">Especifica si el objeto <strong>Parameter</strong> representa un parámetro de entrada, un parámetro de salida o ambos, o si el parámetro es el valor devuelto de un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-176">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-177"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-177"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-178">Especifica el formato en que se guardará un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-178">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-179"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-179"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-180">Especifica la posición actual del puntero de registro dentro de un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-180">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-181"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-182">Especifica los atributos de un objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-182">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-183"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-184">Especifica, para el método <strong>Open</strong> del objeto <strong>Record</strong>, si se debe abrir un <strong>Record</strong> existente o crear un nuevo <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-184">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-185"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-186">Especifica opciones para abrir un <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-186">Specifies options for opening a <strong>Record</strong>.</span></span> <span data-ttu-id="2d8b0-187">Estos valores se pueden combinar utilizando un operador OR.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-187">These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-188"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-189">Especifica el estado de un registro con respecto a actualizaciones por lotes y otras operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-189">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-190"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-191">Especifica el tipo de objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-191">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-192"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-192"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-193">Especifica si los valores subyacentes se sobrescriben con una llamada a <strong>Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-193">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-194"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-p103">Especifica si un archivo se debe crear o sobrescribir al guardar desde un objeto <strong>Stream</strong>. Los valores se pueden combinar con un operador AND (Y).</span><span class="sxs-lookup"><span data-stu-id="2d8b0-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-197"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-197"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-198">Especifica el tipo de esquema <strong>Recordset</strong> recuperado por el método <strong>OpenSchema</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-198">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves.</span></span> <span data-ttu-id="2d8b0-199">Especifica la dirección de un registro dentro de un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-199">Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-200"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-201">Especifica la dirección de una búsqueda de registro dentro de un objeto <strong>Recordset</strong>. Especifica el tipo de búsqueda (<strong>Seek</strong>) que se debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-201">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-202"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-202"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-p105">Especifica el tipo de búsqueda <strong>Seek</strong> que se va a ejecutar. Especifica opciones para abrir un objeto <strong>Stream</strong>. Los valores se pueden combinar con un operador AND.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-p105">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-205"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-p106">Especifica opciones para abrir un objeto <strong>Stream</strong>. Los valores se pueden combinar con un operador AND. Especifica si se debe leer toda la secuencia o la línea siguiente de un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-p106">Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-208"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-208"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-209">Especifica si se debe leer toda la secuencia o la línea siguiente de un objeto <strong>Stream</strong>. Especifica el tipo de datos almacenados en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-209">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-210"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-211">Especifica el tipo de datos almacenado en un objeto <strong>Stream</strong>. Especifica si se agrega un separador de línea a la cadena escrita en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-211">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-212"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-213">Especifica si se agrega un separador de línea a la cadena escrita en el objeto <strong>Stream</strong>. Especifica el formato que se aplica al recuperar un objeto <strong>Recordset</strong> como cadena.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-213">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d8b0-214"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-214"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-215">Especifica el formato que se aplica al recuperar un objeto <strong>Recordset</strong> como cadena. Especifica los atributos de transacción de un objeto <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-215">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d8b0-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="2d8b0-216"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="2d8b0-217">Especifica los atributos de transacción de un objeto <strong> Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d8b0-217">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

