---
title: Cambio previo (evento de macro)
TOCTitle: Before Change macro event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b37fb96ddfeaabc97c6f445f8951876e8026fbfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296860"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="e46ec-102">Cambio previo (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="e46ec-102">Before Change macro event</span></span>

<span data-ttu-id="e46ec-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e46ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e46ec-104">El evento **Cambio previo** se produce cuando cambia un registro, pero antes de confirmar el cambio.</span><span class="sxs-lookup"><span data-stu-id="e46ec-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="e46ec-105">El evento **Cambio previo** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="e46ec-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="e46ec-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e46ec-106">Remarks</span></span>

<span data-ttu-id="e46ec-p101">Utilice el evento **Cambio previo** para realizar cualquier acción que desee que ocurra antes de cambiar un registro. **Cambio previo** se suele utilizar para realizar la validación y para provocar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="e46ec-p101">Use the **Before Change** event to perform any actions that you want to occur before a record is changed. The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="e46ec-109">Puede usar la función **actualizada ("*nombre de campo*")** para determinar si un campo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e46ec-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="e46ec-110">En el ejemplo de código siguiente se muestra cómo usar una instrucción **If** para determinar si se ha modificado el campo el paidinfull.</span><span class="sxs-lookup"><span data-stu-id="e46ec-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="e46ec-p103">Utilice la propiedad **EsInsertar** para determinar si el evento **Cambio previo** se desencadenó por la creación de un nuevo registro o por un cambio en un registro existente. La propiedad **EsInsertar** contiene **Verdadero** si el evento se desencadenó por un nuevo registro y **Falso** si el evento se desencadenó por un cambio en un registro existente.</span><span class="sxs-lookup"><span data-stu-id="e46ec-p103">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record. They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="e46ec-113">En el ejemplo de código siguiente se muestra la sintaxis para utilizar la propiedad **EsInsertar**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="e46ec-114">Puede obtener acceso al valor anterior de un campo mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="e46ec-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="e46ec-115">Por ejemplo, para tener acceso al valor anterior del campo QuantityInStock, utilice la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="e46ec-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="e46ec-116">Los valores anteriores se eliminan permanentemente cuando finaliza el evento **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="e46ec-p104">Puede cancelar el evento **Cambio previo** mediante la acción **ProvocarError**. Cuando se provoca un error se descartan los cambios incluidos en el evento **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-p104">You can cancel the **Before Change** event by using the **RaiseError** action. When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="e46ec-119">La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-119">The following table lists macro commands that can be used in the**Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e46ec-120">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="e46ec-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="e46ec-121">Command</span><span class="sxs-lookup"><span data-stu-id="e46ec-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e46ec-122">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="e46ec-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="e46ec-123"><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e46ec-124">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="e46ec-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="e46ec-125"><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-125"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e46ec-126">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="e46ec-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="e46ec-127"><a href="if-then-else-macro-block.md">If...Then...Else (bloque de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-127"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e46ec-128">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="e46ec-129"><a href="lookuprecord-data-block.md">LookupRecord (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-129"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e46ec-130">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e46ec-131"><a href="clearmacroerror-macro-action.md">BorrarErrorDeMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e46ec-132">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e46ec-133"><a href="onerror-macro-action.md">AlOcurrirError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-133"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e46ec-134">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e46ec-135"><a href="raiseerror-macro-action.md">ProvocarError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-135"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e46ec-136">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e46ec-137"><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-137"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e46ec-138">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e46ec-139"><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-139"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e46ec-140">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="e46ec-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e46ec-141"><a href="stopmacro-macro-action.md">DetenerMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="e46ec-141"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e46ec-142">Para crear una macro de datos que capture el evento **Cambio previo**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e46ec-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="e46ec-143">Abra la tabla en la que desee capturar el evento **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="e46ec-144">En la ficha **Tabla**, en el grupo **Eventos anteriores**, haga clic en **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="e46ec-145">Una macro de datos vacía se muestra en el Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="e46ec-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="e46ec-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e46ec-146">Example</span></span>

<span data-ttu-id="e46ec-147">En el ejemplo de código siguiente se utiliza el evento **cambio previo** para validar los campos de estado.</span><span class="sxs-lookup"><span data-stu-id="e46ec-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="e46ec-148">Se produce un error si el campo Resolución contiene un valor inadecuado.</span><span class="sxs-lookup"><span data-stu-id="e46ec-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

<span data-ttu-id="e46ec-149">Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e46ec-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="e46ec-150">Abra la tabla en la que desee capturar el evento **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="e46ec-151">En la ficha **Tabla**, en el grupo **Eventos anteriores**, haga clic en **Cambio previo**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="e46ec-152">Seleccione el código en el siguiente ejemplo de código y, a continuación, presione **Ctrl + C** para copiarlo en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e46ec-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="e46ec-153">Active la ventana del diseñador de macros y, a continuación, presione **Ctrl + V**.</span><span class="sxs-lookup"><span data-stu-id="e46ec-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

<span data-ttu-id="e46ec-154">En el ejemplo siguiente se muestra cómo usar la acción Provocarerror para cancelar el evento de macro de datos de cambio previo.</span><span class="sxs-lookup"><span data-stu-id="e46ec-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="e46ec-155">Cuando se actualiza el campo AssignedTo, se usa un bloque de datos LookupRecord para determinar si el técnico asignado está actualmente asignado a una solicitud de servicio abierta.</span><span class="sxs-lookup"><span data-stu-id="e46ec-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="e46ec-156">Si es true, se cancela el evento cambio previo y no se actualiza el registro.</span><span class="sxs-lookup"><span data-stu-id="e46ec-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="e46ec-157">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e46ec-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
