---
title: Bloque de datos LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734213"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="34a93-102">Bloque de datos LookupRecord</span><span class="sxs-lookup"><span data-stu-id="34a93-102">LookupRecord data block</span></span>

<span data-ttu-id="34a93-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34a93-104">Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico.</span><span class="sxs-lookup"><span data-stu-id="34a93-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="34a93-105">El bloque de datos **BuscarRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="34a93-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="34a93-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="34a93-106">Setting</span></span>

<span data-ttu-id="34a93-107">La acción **EstablecerCampo** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="34a93-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34a93-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="34a93-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="34a93-109">Necesario</span><span class="sxs-lookup"><span data-stu-id="34a93-109">Required</span></span></p></th>
<th><p><span data-ttu-id="34a93-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="34a93-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a93-111">Hacia dentro</span><span class="sxs-lookup"><span data-stu-id="34a93-111">In</span></span></p></td>
<td><p><span data-ttu-id="34a93-112">Sí</span><span class="sxs-lookup"><span data-stu-id="34a93-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="34a93-113">Una cadena que identifica el registro en el que se operará.</span><span class="sxs-lookup"><span data-stu-id="34a93-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="34a93-114">El <em>argumento In</em> puede contener el nombre de la tabla, una consulta select o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="34a93-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="34a93-115"><strong>NOTA:</strong>El registro especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="34a93-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a93-116">Condición WHERE</span><span class="sxs-lookup"><span data-stu-id="34a93-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="34a93-117">No</span><span class="sxs-lookup"><span data-stu-id="34a93-117">No</span></span></p></td>
<td><p><span data-ttu-id="34a93-118">Una expresión de cadena que se utiliza para restringir el intervalo de datos en el que se ejecuta el bloque de datos <strong>BuscarRegistro</strong>.</span><span class="sxs-lookup"><span data-stu-id="34a93-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="34a93-119">Por ejemplo, los criterios suelen ser equivalentes a la cláusula WHERE en una SQL expresión, sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="34a93-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="34a93-120">Si se omiten criterios, el bloque de datos <strong>LookupRecord</strong> funciona en todo el dominio especificado por el <em>argumento In.</em></span><span class="sxs-lookup"><span data-stu-id="34a93-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="34a93-121">Cualquier campo que se incluya en los criterios debe ser también un campo del argumento <em>En</em>.</span><span class="sxs-lookup"><span data-stu-id="34a93-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a93-122">Alias</span><span class="sxs-lookup"><span data-stu-id="34a93-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="34a93-123">No</span><span class="sxs-lookup"><span data-stu-id="34a93-123">No</span></span></p></td>
<td><p><span data-ttu-id="34a93-124">Cadena que proporciona un nombre alternativo para el registro especificado por el <em>argumento In.</em></span><span class="sxs-lookup"><span data-stu-id="34a93-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="34a93-125">Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas.</span><span class="sxs-lookup"><span data-stu-id="34a93-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="34a93-126">Si no se especifica ningún <em>Alias</em>, se utilizará el nombre de la tabla o consulta como el alias.</span><span class="sxs-lookup"><span data-stu-id="34a93-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="34a93-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34a93-127">Remarks</span></span>

<span data-ttu-id="34a93-128">Si los criterios especificados por los argumentos *In* y *Where Condition* devuelven más de un registro, el bloque de datos **LookupRecord** solo funcionará en el primer registro.</span><span class="sxs-lookup"><span data-stu-id="34a93-128">If the criteria specified by the *In* and *Where Condition* arguments returns more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>  <span data-ttu-id="34a93-129">En el caso de que ningún registro coincida con los criterios especificados, Access omitirá el conjunto de acciones contenidas en el bloque **LookupRecord,** como si hubiera sido una expresión de bloque de macro **[If](if-then-else-macro-block.md)** que se evaluó como false.</span><span class="sxs-lookup"><span data-stu-id="34a93-129">In the case that no records match the specified criteria, Access will skip over the set of actions contained within the **LookupRecord** block, as if it had been an **[If](if-then-else-macro-block.md)** macro block expression that evaluated as false.</span></span>

## <a name="example"></a><span data-ttu-id="34a93-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34a93-130">Example</span></span>

<span data-ttu-id="34a93-131">En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor de una macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="34a93-131">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="34a93-132">Se devuelve una clase ReturnVar denominada **CurrentServiceRequest** a la subrutina Visual Basic para Aplicaciones (VBA) que llamó a la macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="34a93-132">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="34a93-133">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="34a93-133">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

<span data-ttu-id="34a93-134">En el ejemplo siguiente se muestra cómo usar la acción RaiseError para cancelar el evento de macro de datos Before Change.</span><span class="sxs-lookup"><span data-stu-id="34a93-134">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="34a93-135">Cuando se actualiza el campo AssignedTo, se usa un bloque de datos LookupRecord para determinar si el técnico asignado está asignado actualmente a una solicitud de servicio abierta.</span><span class="sxs-lookup"><span data-stu-id="34a93-135">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="34a93-136">Si esto es así, el evento Before Change se cancela y el registro no se actualiza.</span><span class="sxs-lookup"><span data-stu-id="34a93-136">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
