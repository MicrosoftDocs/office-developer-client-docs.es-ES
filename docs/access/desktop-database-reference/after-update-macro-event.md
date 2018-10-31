---
title: Después de actualizar (evento de macro)
TOCTitle: After Update Macro Event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6c4e854e13527f0c20551950aa49dde30cdae9ab
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862264"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="f5b55-102">Después de actualizar (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="f5b55-102">After Update Macro Event</span></span>


<span data-ttu-id="f5b55-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5b55-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f5b55-104">El evento **Después de actualizar** se produce después de actualizar un registro.</span><span class="sxs-lookup"><span data-stu-id="f5b55-104">The **After Update** event occurs after a record is changed.</span></span>


> [!NOTE]
> <span data-ttu-id="f5b55-105">[!NOTA] El evento **Después de actualizar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="f5b55-105">The **After Update** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="f5b55-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5b55-106">Remarks</span></span>

<span data-ttu-id="f5b55-p101">Utilice el evento **Después de actualizar** para realizar cualquier acción que desee que se produzca cuando se cambia un registro. **Después de actualizar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="f5b55-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="f5b55-p102">Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo utilizar una instrucción **If** para determinar si se ha cambiado el campo PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="f5b55-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="f5b55-111">Puede obtener acceso al valor anterior de un campo mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="f5b55-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="f5b55-112">Por ejemplo, para tener acceso al valor anterior del campo QuantityInStock, utilice la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="f5b55-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="f5b55-113">Los valores anteriores se eliminan permanentemente cuando finaliza el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5b55-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="f5b55-114">La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5b55-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5b55-115">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="f5b55-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="f5b55-116">Comando</span><span class="sxs-lookup"><span data-stu-id="f5b55-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-117">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="f5b55-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="f5b55-118"><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-119">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="f5b55-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="f5b55-120"><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-121">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="f5b55-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="f5b55-122"><a href="if-then-else-macro-block.md">Si...Entonces...Sino (bloque de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-123">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="f5b55-124"><a href="createrecord-data-block.md">CrearRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-124"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-125">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="f5b55-126"><a href="editrecord-data-block.md">EditarRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-126"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-127">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="f5b55-128"><a href="foreachrecord-data-block.md">ParaCadaRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-128"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-129">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="f5b55-130"><a href="lookuprecord-data-block.md">BuscarRegistro (bloque de datos)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-131">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-132"><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-133">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-134"><a href="clearmacroerror-macro-action.md">BorrarErrorDeMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-134"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-135">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-136"><a href="deleterecord-macro-action.md">EliminarRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-136"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-137">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-138"><a href="exitforeachrecord-macro-action.md">SalirDeCadaRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-139">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-140"><a href="logevent-macro-action.md">RegistrarEvento (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-140"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-141">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-142"><a href="onerror-macro-action.md">AlOcurrirError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-142"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-143">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-144"><a href="raiseerror-macro-action.md">ProvocarError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-144"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-145">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-146"><a href="rundatamacro-macro-action.md">EjecutarMacroDeDatos (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-146"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-147">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-148"><a href="sendemail-macro-action.md">EnviarCorreoElectrónico (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-148"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-149">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-150"><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-150"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-151">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-152"><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-152"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5b55-153">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-154"><a href="stopallmacros-macro-action.md">DetenerTodasMacros (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-154"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5b55-155">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="f5b55-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f5b55-156"><a href="stopmacro-macro-action.md">DetenerMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="f5b55-156"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f5b55-157">Para crear una macro de datos que capture el evento **Después de actualizar**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5b55-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="f5b55-158">Abra la tabla en la que desee capturar el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5b55-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="f5b55-159">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5b55-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="f5b55-160">Una macro de datos vacía se muestra en el Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="f5b55-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="f5b55-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5b55-161">Example</span></span>

<span data-ttu-id="f5b55-162">En el ejemplo de código siguiente se utiliza el evento **Después de actualizar** para ejecutar una macro de datos con nombre que agrega un registro a la tabla Comentario cada vez que se actualiza el estado de un problema.</span><span class="sxs-lookup"><span data-stu-id="f5b55-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="f5b55-163">**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**</span><span class="sxs-lookup"><span data-stu-id="f5b55-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="f5b55-164">Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5b55-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="f5b55-165">Abra la tabla en la que desee capturar el evento **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5b55-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="f5b55-166">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de actualizar**.</span><span class="sxs-lookup"><span data-stu-id="f5b55-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="f5b55-167">Seleccione el código en el siguiente ejemplo de código y, a continuación, presione CTRL+C para copiarlo al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="f5b55-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="f5b55-168">Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="f5b55-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

