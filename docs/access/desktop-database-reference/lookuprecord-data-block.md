---
title: Bloque de datos BuscarRegistro
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c93f312dd9b43a3235f049b9e6d3f95d08eba87f
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025598"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="068f6-102">Bloque de datos BuscarRegistro</span><span class="sxs-lookup"><span data-stu-id="068f6-102">LookupRecord data block</span></span>

<span data-ttu-id="068f6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="068f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="068f6-104">Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico.</span><span class="sxs-lookup"><span data-stu-id="068f6-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="068f6-105">[!NOTA] El bloque de datos **BuscarRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="068f6-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="068f6-106">Valores</span><span class="sxs-lookup"><span data-stu-id="068f6-106">Setting</span></span>

<span data-ttu-id="068f6-107">La acción **EstablecerCampo** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="068f6-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="068f6-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="068f6-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="068f6-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="068f6-109">Required</span></span></p></th>
<th><p><span data-ttu-id="068f6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="068f6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="068f6-111">In</span><span class="sxs-lookup"><span data-stu-id="068f6-111">In</span></span></p></td>
<td><p><span data-ttu-id="068f6-112">Sí</span><span class="sxs-lookup"><span data-stu-id="068f6-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="068f6-113">Una cadena que identifica el registro para funcionar en.</span><span class="sxs-lookup"><span data-stu-id="068f6-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="068f6-114">El argumento <em>en</em> puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="068f6-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="068f6-115"><strong>Nota</strong>: el registro especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="068f6-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068f6-116">Condición WHERE</span><span class="sxs-lookup"><span data-stu-id="068f6-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="068f6-117">No</span><span class="sxs-lookup"><span data-stu-id="068f6-117">No</span></span></p></td>
<td><p><span data-ttu-id="068f6-118">Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos <strong>BuscarRegistro</strong> se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="068f6-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="068f6-119">Por ejemplo, criterios suelen ser equivalentes a la cláusula WHERE en una expresión SQL, sin la palabra donde.</span><span class="sxs-lookup"><span data-stu-id="068f6-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="068f6-120">Si se omiten criterios, el bloque de datos <strong>BuscarRegistro</strong> funciona en todo el dominio especificado por el argumento <em>en</em> .</span><span class="sxs-lookup"><span data-stu-id="068f6-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="068f6-121">Cualquier campo que se incluya en criterios debe ser también un campo de <em>en</em>.</span><span class="sxs-lookup"><span data-stu-id="068f6-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068f6-122">Alias</span><span class="sxs-lookup"><span data-stu-id="068f6-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="068f6-123">No</span><span class="sxs-lookup"><span data-stu-id="068f6-123">No</span></span></p></td>
<td><p><span data-ttu-id="068f6-124">Una cadena que proporciona un nombre alternativo para el registro especificado por el argumento <em>en</em> .</span><span class="sxs-lookup"><span data-stu-id="068f6-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="068f6-125">A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas.</span><span class="sxs-lookup"><span data-stu-id="068f6-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="068f6-126">Si no se especifica ningún <em>Alias</em>, se utilizará el nombre de la tabla o consulta como el alias.</span><span class="sxs-lookup"><span data-stu-id="068f6-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="068f6-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="068f6-127">Remarks</span></span>

<span data-ttu-id="068f6-128">Si los criterios especificados por los argumentos *en* y *Condición Where* especifica más de un registro, el bloque de datos **BuscarRegistro** funcionará sólo en el primer registro.</span><span class="sxs-lookup"><span data-stu-id="068f6-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="068f6-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="068f6-129">Example</span></span>

<span data-ttu-id="068f6-130">En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor desde una macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="068f6-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="068f6-131">Un ReturnVar denominado **CurrentServiceRequest** se devuelve a la macro o Visual Basic para la subrutina de aplicaciones (VBA) que llama a la macro de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="068f6-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="068f6-132">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="068f6-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="068f6-133">En el ejemplo siguiente se muestra cómo usar la acción Provocarerror para cancelar el evento de macro de datos antes de cambiar.</span><span class="sxs-lookup"><span data-stu-id="068f6-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="068f6-134">Cuando se actualiza el campo AssignedTo, un bloque de datos BuscarRegistro se usa para determinar si el técnico asignado actualmente está asignado a una solicitud de servicio abiertas.</span><span class="sxs-lookup"><span data-stu-id="068f6-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="068f6-135">Si es true, se cancela el evento cambio previo y no se actualiza el registro.</span><span class="sxs-lookup"><span data-stu-id="068f6-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
