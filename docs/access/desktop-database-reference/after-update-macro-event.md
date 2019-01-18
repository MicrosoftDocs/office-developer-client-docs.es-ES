---
title: Después de actualizar (evento de macro)
TOCTitle: After Update macro event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a96b46fcc78c4f93887e487f52091a77da6c0d2f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699460"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="a55fe-102">Después de actualizar (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="a55fe-102">After Update macro event</span></span>

<span data-ttu-id="a55fe-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a55fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a55fe-104">El evento **Después de actualizar** se produce después de actualizar un registro.</span><span class="sxs-lookup"><span data-stu-id="a55fe-104">The **After Update** event occurs after a record is changed.</span></span>

> [!NOTE]
> <span data-ttu-id="a55fe-105">[!NOTA] El evento **Después de actualizar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="a55fe-105">The **After Update** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="a55fe-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a55fe-106">Remarks</span></span>

<span data-ttu-id="a55fe-p101">Utilice el evento **Después de actualizar** para realizar cualquier acción que desee que se produzca cuando se cambia un registro. **Después de actualizar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a55fe-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="a55fe-p102">Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo utilizar una instrucción **If** para determinar si se ha cambiado el campo PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="a55fe-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="a55fe-111">Puede obtener acceso al valor anterior de un campo mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="a55fe-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="a55fe-112">Por ejemplo, para tener acceso al valor anterior del campo QuantityInStock, utilice la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="a55fe-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="a55fe-113">Los valores anteriores se eliminan permanentemente cuando finaliza el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a55fe-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="a55fe-114">La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a55fe-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a55fe-115">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="a55fe-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="a55fe-116">Comando</span><span class="sxs-lookup"><span data-stu-id="a55fe-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-117">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="a55fe-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="a55fe-118"><a href="comment-macro-statement.md">Instrucción de macro de comentario</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-119">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="a55fe-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="a55fe-120"><a href="group-macro-statement.md">Instrucción de macro de grupo</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-121">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="a55fe-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="a55fe-122"><a href="if-then-else-macro-block.md">If... A continuación... Bloque de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-123">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="a55fe-124"><a href="createrecord-data-block.md">Acción de macro CrearRegistro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-124"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-125">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="a55fe-126"><a href="editrecord-data-block.md">Acción de macro EditarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-126"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-127">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="a55fe-128"><a href="foreachrecord-data-block.md">Acción de macro ParaCadaRegistro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-128"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-129">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="a55fe-130"><a href="lookuprecord-data-block.md">Bloque de datos BuscarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-130"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-131">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-132"><a href="cancelrecordchange-macro-action.md">Acción de macro CancelarCambioDeRegistro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-133">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-134"><a href="clearmacroerror-macro-action.md">Acción de macro BorrarErrorDeMacro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-135">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-136"><a href="deleterecord-macro-action.md">Acción de macro DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-137">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-138"><a href="exitforeachrecord-macro-action.md">Acción de macro Salirdecadaregistro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-139">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-140"><a href="logevent-macro-action.md">Acción de macro LogEvent</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-141">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-142"><a href="onerror-macro-action.md">Acción de macro AlOcurrirError</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-143">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-144"><a href="raiseerror-macro-action.md">Acción de macro Provocarerror</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-145">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-146"><a href="rundatamacro-macro-action.md">Acción de macro EjecutarMacroDeDatos</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-147">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-148"><a href="sendemail-macro-action.md">Acción de macro EnviarCorreoElectrónico</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-149">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-150"><a href="setfield-macro-action.md">Acción de macro SetField</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-151">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-152"><a href="setlocalvar-macro-action.md">Acción de macro EstablecerVariableLocal</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55fe-153">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-154"><a href="stopallmacros-macro-action.md">Acción de macro DetenerTodasMacros</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55fe-155">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="a55fe-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="a55fe-156"><a href="stopmacro-macro-action.md">Acción de macro DetenerMacro</a></span><span class="sxs-lookup"><span data-stu-id="a55fe-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a55fe-157">Para crear una macro de datos que capture el evento **Después de actualizar**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a55fe-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="a55fe-158">Abra la tabla en la que desee capturar el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a55fe-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="a55fe-159">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a55fe-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="a55fe-160">Una macro de datos vacía se muestra en el Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="a55fe-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="a55fe-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a55fe-161">Example</span></span>

<span data-ttu-id="a55fe-162">En el ejemplo de código siguiente se utiliza el evento **Después de actualizar** para ejecutar una macro de datos con nombre que agrega un registro a la tabla Comentario cada vez que se actualiza el estado de un problema.</span><span class="sxs-lookup"><span data-stu-id="a55fe-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="a55fe-163">**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**</span><span class="sxs-lookup"><span data-stu-id="a55fe-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="a55fe-164">Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a55fe-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="a55fe-165">Abra la tabla en la que desee capturar el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a55fe-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="a55fe-166">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="a55fe-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="a55fe-167">Seleccione el código en el siguiente ejemplo de código y, a continuación, presione CTRL+C para copiarlo al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="a55fe-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="a55fe-168">Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="a55fe-168">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterUpdate"> 
        <Statements> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Status")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Status changed to &quot; &amp; [Status]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Resolution")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Issue resolved as &quot; &amp; [Resolution]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
``` 

<br/>

```vb
If  Updated("Status")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
         prmComment   ="--Status Changes to "&[Status] 
          prmUserID   =[ChangedByUserID] 
End If 
 
If   Updated("Resolution")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
          prmUserID   =[ChangedByUserID] 
         prmComment   ="--Issue Resolved as "&[Status] 
End If 
```

