---
title: Referencia de errores en ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717240"
---
# <a name="ado-error-reference"></a><span data-ttu-id="c65d9-102">Referencia de errores en ADO</span><span class="sxs-lookup"><span data-stu-id="c65d9-102">ADO error reference</span></span>

<span data-ttu-id="c65d9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c65d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c65d9-p101">La constante **ErrorValueEnum** describe los valores de error en ADO. Para consultar una lista completa de estas constantes enumeradas, incluyendo sus valores, vea [Apéndice B: Errores de ADO](appendix-b-ado-errors.md). En esta sección, se examinan algunos de los errores más interesantes y se explican algunas situaciones específicas que pueden causarlos, o soluciones para corregir el problema. Se indica la constante **ErrorValueEnum** y el número decimal positivo corto.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p101">The **ErrorValueEnum** constant describes the ADO error values. For a complete listing of these enumerated constants, including values, see [Appendix B: ADO Errors](appendix-b-ado-errors.md). This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem. Both the **ErrorValueEnum** constant and the short positive decimal number are listed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c65d9-108">Número</span><span class="sxs-lookup"><span data-stu-id="c65d9-108">Number</span></span></p></th>
<th><p><span data-ttu-id="c65d9-109">Constante ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="c65d9-109">ErrorValueEnum constant</span></span></p></th>
<th><p><span data-ttu-id="c65d9-110">Descripción/Causas posibles</span><span class="sxs-lookup"><span data-stu-id="c65d9-110">Description/Possible causes</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-111"><strong>3000</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-111"><strong>3000</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-112"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-112"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-113">El proveedor no pudo realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="c65d9-113">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-114"><strong>3001</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-114"><strong>3001</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-115"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-115"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p102">Los argumentos son del tipo incorrecto, están fuera del intervalo aceptable o están en conflicto entre sí. Este error se produce a menudo por un error tipográfico en una instrucción SQL SELECT. Por ejemplo, un nombre de campo o de tabla mal escrito puede generar este error. Este error también se puede producir cuando no existe en el almacén de datos un campo o una tabla que se menciona en una instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p102">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another. This error is often caused by a typographical error in an SQL SELECT statement. For example, a misspelled field name or table name can generate this error. This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-120"><strong>3002</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-120"><strong>3002</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-121"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-121"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p103">No se pudo abrir un archivo. Se especificó un nombre de archivo mal escrito, o se movió, cambió o eliminó un archivo. En una red, podría ser que la unidad no estuviese disponible temporalmente o que el tráfico en la red impidiese una conexión.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p103">File could not be opened. A misspelled file name was specified, or a file has been moved, renamed, or deleted. Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-125"><strong>3003</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-125"><strong>3003</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-126"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-126"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p104">No se pudo leer un archivo. El nombre del archivo se ha especificado incorrectamente, el archivo se puede haber movido o eliminado, o el archivo se puede haber dañado.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p104">File could not be read. The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-129"><strong>3004</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-129"><strong>3004</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-130"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-130"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p105">Error de escritura en un archivo. Tal vez haya cerrado un archivo y después intentado escribir en él, o el archivo podría estar dañado. Si el archivo está en una unidad de red, ciertas condiciones transitorias de la red podrían impedir la escritura en una unidad de red.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p105">Write to file failed. You might have closed a file and then tried to write to it, or the file might be corrupted. If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-134"><strong>3021</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-134"><strong>3021</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-135"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-135"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p106"><strong>BOF</strong> o <strong>EOF</strong> es True, o bien el registro actual se ha eliminado. La operación solicitada requiere un registro actual. Se realizó un intento de actualizar registros mediante <strong>Find</strong> o <strong>Seek</strong> para mover el puntero de registros al registro deseado. Si no se encuentra el registro, <strong>EOF</strong> será True. Este error también se puede producir después de un error de <strong>AddNew</strong> o <strong>Delete</strong> porque, cuando estos métodos generan errores, no hay registro activo.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p106">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record. An attempt was made to update records by using <strong>Find</strong> or <strong>Seek</strong> to move the record pointer to the desired record. If the record is not found, <strong>EOF</strong> will be True. This error can also occur after a failed <strong>AddNew</strong> or <strong>Delete</strong> because there is no current record when these methods fail.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-141"><strong>3219</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-141"><strong>3219</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-142"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-142"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-143">Operación no permitida en este contexto.</span><span class="sxs-lookup"><span data-stu-id="c65d9-143">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-144"><strong>3220</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-144"><strong>3220</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-145"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-145"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-146">El proveedor suministrado es distinto del que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="c65d9-146">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-147"><strong>3246</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-147"><strong>3246</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-148"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-148"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p107">No se puede cerrar explícitamente un objeto <strong>Connection</strong> durante una transacción. No se puede cerrar un objeto <strong>Recordset</strong> o <strong>Connection</strong> que esté participando en una transacción. Llame a <strong>RollbackTrans</strong> o a <strong>CommitTrans</strong> antes de cerrar el objeto.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p107"><strong>Connection</strong> object cannot be explicitly closed while in a transaction. A <strong>Recordset</strong> or <strong>Connection</strong> object that is currently participating in a transaction cannot be closed. Call either <strong>RollbackTrans</strong> or <strong>CommitTrans</strong> before closing the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-152"><strong>3251</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-152"><strong>3251</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-153"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-153"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p108">El objeto o el proveedor no es capaz de realizar la operación solicitada. Algunas operaciones dependen de una versión de proveedor determinada.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p108">The object or provider is not capable of performing the requested operation. Some operations depend on a particular provider version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-156"><strong>3265</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-156"><strong>3265</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-157"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-157"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p109">No se puede encontrar un elemento en la colección correspondiente al nombre o el ordinal solicitado. Se ha especificado un nombre de campo o de tabla incorrecto.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p109">Item cannot be found in the collection corresponding to the requested name or ordinal. An incorrect field or table name has been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-160"><strong>3367</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-160"><strong>3367</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-161"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-161"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p110">El objeto ya está en la colección. No se puede anexar. Un objeto no se puede agregar dos veces a la misma colección.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p110">Object is already in collection. Cannot append. An object cannot be added to the same collection twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-165"><strong>3420</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-165"><strong>3420</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-166"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-166"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-167">El objeto ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="c65d9-167">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-168"><strong>3421</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-168"><strong>3421</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-169"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-169"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p111">La aplicación utiliza un valor de tipo incorrecto para la operación actual. Tal vez haya proporcionado una cadena a una operación que espera, por ejemplo, una secuencia.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p111">Application uses a value of the wrong type for the current operation. You might have supplied a string to an operation that expects a stream, for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-172"><strong>3704</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-172"><strong>3704</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-173"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-173"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p112">La operación no está permitida si el objeto está cerrado. Se cerró <strong>Connection</strong> o <strong>Recordset</strong>. Por ejemplo, puede ser que alguna otra rutina haya cerrado un objeto global. Este error se puede evitar comprobando la propiedad <strong>State</strong> antes de intentar realizar una operación.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p112">Operation is not allowed when the object is closed. The <strong>Connection</strong> or <strong>Recordset</strong> has been closed. For example, some other routine might have closed a global object. You can prevent this error by checking the <strong>State</strong> property before you attempt an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-178"><strong>3705</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-178"><strong>3705</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-179"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-179"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p113">La operación no está permitida si el objeto está abierto. No se puede abrir un objeto que ya está abierto. No se pueden anexar campos a un <strong>conjunto de registros</strong> abierto.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p113">Operation is not allowed when the object is open. An object that is open cannot be opened. Fields cannot be appended to an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-183"><strong>3706</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-183"><strong>3706</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-184"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-184"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p114">No se encuentra el proveedor. Puede que no esté instalado correctamente. Tal vez no se haya especificado correctamente el nombre del proveedor, o no se haya instalado el proveedor especificado en el equipo donde se está ejecutando el código, o se haya dañado la instalación.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p114">Provider cannot be found. It may not be properly installed. The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-188"><strong>3707</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-188"><strong>3707</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-189"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-189"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p115">No se puede cambiar la propiedad <strong>ActiveConnection</strong> de un objeto <strong>Recordset</strong> que tiene un objeto <strong>Command</strong> como origen. La aplicación intentó asignar un objeto <strong>Connection</strong> nuevo a un <strong>conjunto de registros</strong> que tiene un objeto <strong>Command</strong> como origen.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p115">The <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object, which has a <strong>Command</strong> object as its source, cannot be changed. The application attempted to assign a new <strong>Connection</strong> object to a <strong>Recordset</strong> that has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-192"><strong>3708</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-192"><strong>3708</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-193"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-193"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p116">El objeto <strong>Parameter</strong> no se ha definido correctamente. Se proporcionó información incoherente o incompleta.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p116"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-196"><strong>3709</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-196"><strong>3709</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-197"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-197"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p117">No se puede utilizar la conexión para realizar esta operación. Está cerrada o no es válida en este contexto.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p117">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-200"><strong>3710</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-200"><strong>3710</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-201"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-201"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p118">No se puede realizar la operación mientras se procesa el evento. No se puede realizar una operación dentro de un controlador de eventos que provoca que se desencadene el evento de nuevo. Por ejemplo, no se debe llamar a métodos de navegación desde dentro de un controlador de eventos <strong>WillMove</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p118">Operation cannot be performed while processing event. An operation cannot be performed within an event handler that causes the event to fire again. For example, navigation methods should not be called from within a <strong>WillMove</strong> event handler.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-205"><strong>3711</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-205"><strong>3711</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-206"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-206"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-207">No se puede realizar la operación mientras se ejecuta asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="c65d9-207">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-208"><strong>3712</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-208"><strong>3712</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-209"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-209"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p119">La operación ha sido cancelada por el usuario. La aplicación ha llamado al método <strong>CancelUpdate</strong> o <strong>CancelBatch</strong> y se ha cancelado la operación en curso.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p119">Operation has been canceled by the user. The application has called the <strong>CancelUpdate</strong> or <strong>CancelBatch</strong> method and the current operation has been canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-212"><strong>3713</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-212"><strong>3713</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-213"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-213"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-214">No se puede realizar la operación mientras se conecta asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="c65d9-214">Operation cannot be performed while connecting asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-215"><strong>3714</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-215"><strong>3714</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-216"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-216"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-217">La transacción de coordinación no es válida o no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="c65d9-217">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-218"><strong>3715</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-218"><strong>3715</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-219"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-219"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-220">No se puede realizar la operación mientras no se ejecute.</span><span class="sxs-lookup"><span data-stu-id="c65d9-220">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-221"><strong>3716</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-221"><strong>3716</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-222"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-222"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-223">La configuración de seguridad de este equipo prohíbe el acceso a un origen de datos en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="c65d9-223">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-224"><strong>3717</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-224"><strong>3717</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-225"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-225"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p120">Para uso interno exclusivamente. No utilizar (la entrada se ha incluido para ofrecer una información completa; este error no debería aparecer en su código).</span><span class="sxs-lookup"><span data-stu-id="c65d9-p120">For internal use only. Don't use. (Entry was included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-230"><strong>3718</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-230"><strong>3718</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-231"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-231"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p121">Para uso interno exclusivamente. No utilizar (entrada incluida para ofrecer una información completa; este error no debería aparecer en su código).</span><span class="sxs-lookup"><span data-stu-id="c65d9-p121">For internal use only. Don't use. (Entry included for the sake of completeness. This error should not appear in your code.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-236"><strong>3719</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-236"><strong>3719</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-237"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-237"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p122">El valor de los datos entra en conflicto con las restricciones de integridad del campo. Un valor nuevo para un <strong>campo</strong> generaría una clave duplicada. Un valor que conforma un lado de una relación entre dos registros podría no ser actualizable.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p122">Data value conflicts with the integrity constraints of the field. A new value for a <strong>Field</strong> would cause a duplicate key. A value that forms one side of a relationship between two records might not be updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-241"><strong>3720</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-241"><strong>3720</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-242"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-242"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p123">No se tienen suficientes permisos para escribir en el campo. El usuario mencionado en la cadena de conexión no tiene los permisos apropiados para escribir en un <strong>campo</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p123">Insufficient permission prevents writing to the field. The user named in the connection string does not have the proper permissions to write to a <strong>Field</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-245"><strong>3721</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-245"><strong>3721</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-246"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-246"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p124">El valor de los datos es demasiado grande para poder representarlo mediante el tipo de datos del campo. Se asignó un valor numérico que es demasiado grande para el campo correspondiente. Por ejemplo, un valor entero largo se asignó a un campo numérico entero corto.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p124">Data value is too large to be represented by the field data type. A numeric value that is too large for the intended field was assigned. For example, a long integer value was assigned to a short integer field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-250"><strong>3722</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-250"><strong>3722</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-251"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-251"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p125">El valor de los datos está en conflicto con el tipo de datos o las restricciones del campo. El almacén de datos tiene restricciones de validación que difieren del valor del <strong>campo</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p125">Data value conflicts with the data type or constraints of the field. The data store has validation constraints that differ from the <strong>Field</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-254"><strong>3723</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-254"><strong>3723</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-255"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-255"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-256">La conversión produjo un error porque el valor de los datos tenía signo y el tipo de datos del campo utilizado por el proveedor no tenía signo.</span><span class="sxs-lookup"><span data-stu-id="c65d9-256">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-257"><strong>3724</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-257"><strong>3724</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-258"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-258"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p126">El valor de los datos no se puede convertir por motivos distintos a un desajuste entre signos o a un desbordamiento de datos. Por ejemplo, puede que la conversión haya truncado datos.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p126">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-261"><strong>3725</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-261"><strong>3725</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-262"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-262"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-263">No se puede establecer ni recuperar el valor de los datos porque el tipo de datos del campo era desconocido o el proveedor no tenía suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c65d9-263">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-264"><strong>3726</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-264"><strong>3726</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-265"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-265"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p127">El registro no contiene este campo. Se especificó un nombre de campo incorrecto o se hizo referencia a un campo no incluido en la colección <strong>Fields</strong> del registro activo.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p127">Record does not contain this field. An incorrect field name was specified or a field not in the <strong>Fields</strong> collection of the current record was referenced.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-268"><strong>3727</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-268"><strong>3727</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-269"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-269"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-270">No existe la dirección URL de origen o la dirección URL del elemento principal de destino.</span><span class="sxs-lookup"><span data-stu-id="c65d9-270">Either the source URL or the parent of the destination URL does not exist.</span></span> <span data-ttu-id="c65d9-271">Hay un error tipográfico en la dirección URL de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="c65d9-271">There is a typographical error in either the source or destination URL.</span></span> <span data-ttu-id="c65d9-272">Es posible que deba https://mysite/photo/myphoto.jpg cuando en realidad debiera tener https://mysite/photos/myphoto.jpg en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c65d9-272">You might have https://mysite/photo/myphoto.jpg when you should actually have https://mysite/photos/myphoto.jpg instead.</span></span> <span data-ttu-id="c65d9-273">El error tipográfico en la dirección URL principal (en este caso, <em>photo</em> en vez de <em>photos</em>) ha provocado el error.</span><span class="sxs-lookup"><span data-stu-id="c65d9-273">The typographical error in the parent URL (in this case, <em>photo</em> instead of <em>photos</em>) has caused the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-274"><strong>3728</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-274"><strong>3728</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-275"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-275"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p129">No se tienen suficientes permisos para obtener acceso a un árbol o a un subárbol. El usuario mencionado en la cadena de conexión no tiene los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p129">Permissions are insufficient to access tree or subtree. The user named in the connection string does not have the appropriate permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-278"><strong>3729</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-278"><strong>3729</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-279"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-279"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p130">La dirección URL contiene caracteres no válidos. Asegúrese de que la dirección URL está escrita correctamente. La dirección URL sigue el esquema registrado para el proveedor actual (por ejemplo, Internet Publishing Provider está registrado para http).</span><span class="sxs-lookup"><span data-stu-id="c65d9-p130">URL contains invalid characters. Make sure the URL is typed correctly. The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-283"><strong>3730</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-283"><strong>3730</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-284"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-284"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p131">El objeto representado por la dirección URL especificada está bloqueado por uno o varios procesos diferentes. Espere hasta que el proceso haya finalizado e intente de nuevo la operación. El objeto al que trata de tener acceso ha sido bloqueado por otro usuario o por otro proceso de su aplicación. Esto suele ocurrir en un entorno multiusuario.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p131">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again. The object you are trying to access has been locked by another user or by another process in your application. This is most likely to arise in a multi-user environment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-289"><strong>3731</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-289"><strong>3731</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-290"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-290"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p132">No se puede realizar una operación de copia. El objeto mencionado en la dirección URL de destino ya existe. Especifique <strong>adCopyOverwrite</strong> para reemplazar el objeto. Si no especifica <strong>adCopyOverwrite</strong> cuando copie los archivos a un directorio, se producirá un error al intentar copiar un elemento que ya exista en la ubicación de destino.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p132">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object. If you do not specify <strong>adCopyOverwrite</strong> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-295"><strong>3732</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-295"><strong>3732</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-296"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-296"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p133">El servidor no puede completar la operación. Puede deberse a que el servidor esté ocupado con otras operaciones, o a que tenga un bajo nivel de recursos.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p133">The server cannot complete the operation. This might be because the server is busy with other operations or it might be low on resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-299"><strong>3733</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-299"><strong>3733</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-300"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-300"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p134">El proveedor no puede encontrar el dispositivo de almacenamiento que indica la dirección URL. Compruebe que la dirección URL está escrita correctamente. La dirección URL del dispositivo de almacenamiento podría no ser correcta, pero este error puede deberse a otros motivos. El dispositivo podría estar desconectado, o un elevado volumen de tráfico en la red podría impedir el establecimiento de la conexión.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p134">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly. The URL of the storage device might be incorrect, but this error can occur for other reasons. The device might be offline or a large volume of network traffic might prevent the connection from being made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-305"><strong>3734</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-305"><strong>3734</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-306"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-306"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p135">No se puede realizar operación. El proveedor no puede obtener suficiente espacio de almacenamiento. Podría no haber suficiente memoria RAM o espacio en disco para archivos temporales del servidor.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p135">Operation cannot be performed. Provider cannot obtain enough storage space. There might not be enough RAM or hard-drive space for temporary files on the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-310"><strong>3735</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-310"><strong>3735</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-311"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-311"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-312">La dirección URL de origen o de destino está fuera del alcance del registro activo.</span><span class="sxs-lookup"><span data-stu-id="c65d9-312">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-313"><strong>3736</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-313"><strong>3736</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-314"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-314"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p136">La operación no se pudo completar y el estado no está disponible. Tal vez el campo no esté disponible o no se haya intentado la operación. Otro usuario podría haber cambiado o eliminado el campo al que está intentando obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p136">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted. Another user might have changed or deleted the field you are trying to access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-318"><strong>3737</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-318"><strong>3737</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-319"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-319"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p137">No existe el registro mencionado en esta dirección URL. Al intentar abrir un archivo utilizando un objeto <strong>Record</strong>, no se escribió correctamente el nombre de archivo o la ruta de acceso al archivo.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p137">Record named by this URL does not exist. While attempting to open a file using a <strong>Record</strong> object, either the file name or the path to the file was misspelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-322"><strong>3738</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-322"><strong>3738</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-323"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-323"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-324">La dirección URL del objeto que se va a eliminar está fuera del alcance del registro activo.</span><span class="sxs-lookup"><span data-stu-id="c65d9-324">The URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-325"><strong>3747</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-325"><strong>3747</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-326"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-326"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-327">La operación requiere un <strong>ParentCatalog</strong> válido.</span><span class="sxs-lookup"><span data-stu-id="c65d9-327">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-328"><strong>3748</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-328"><strong>3748</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-329"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-329"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p138">Se denegó la conexión. La conexión nueva que solicitó tiene características diferentes que la que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p138">Connection was denied. The new connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-332"><strong>3749</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-332"><strong>3749</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-333"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-333"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p139">Error en la actualización de campos. Para obtener más información, examine la propiedad <strong>Status</strong> de objetos de campo individuales. Este error puede producirse en dos situaciones: al cambiar el valor de un objeto <strong>Field</strong> durante el proceso de cambio o inclusión de un registro en la base de datos, y al cambiar las propiedades del propio objeto <strong>Field</strong>. Hubo un error en la actualización de <strong>Record</strong> o <strong>Recordset</strong> debido a un problema con uno de los campos en el registro actual. Enumere la colección <strong>Fields</strong> y compruebe la propiedad <strong>Status</strong> de cada campo para determinar la causa del problema.  </span><span class="sxs-lookup"><span data-stu-id="c65d9-p139">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects. This error can occur in two situations: when changing a <strong>Field</strong> object's value in the process of changing or adding a record to the database; and when changing the properties of the <strong>Field</strong> object itself. The <strong>Record</strong> or <strong>Recordset</strong> update failed due to a problem with one of the fields in the current record. Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c65d9-339"><strong>3750</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-339"><strong>3750</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-340"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-340"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p140">El proveedor no admite restricciones compartidas. Se ha realizado un intento de restringir un uso compartido de archivos y su proveedor no admite el concepto.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p140">Provider does not support sharing restrictions. An attempt was made to restrict file sharing and your provider does not support the concept.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c65d9-343"><strong>3751</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-343"><strong>3751</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-344"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="c65d9-344"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="c65d9-p141">El proveedor no admite el tipo restricciones compartidas solicitado. Se realizó un intento de establecer un tipo determinado de restricción de uso compartido de archivos que no admite su proveedor. Vea la documentación del proveedor para determinar qué restricciones de uso compartido de archivos se admiten.</span><span class="sxs-lookup"><span data-stu-id="c65d9-p141">Provider does not support the requested kind of sharing restriction. An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider. See the provider's documentation to determine what file-sharing restrictions are supported.</span></span></p></td>
</tr>
</tbody>
</table>

