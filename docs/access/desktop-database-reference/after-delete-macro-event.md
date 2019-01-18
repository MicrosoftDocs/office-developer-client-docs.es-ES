---
title: Después de eliminar (evento de macro)
TOCTitle: After Delete macro event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f524a544736f68bcfa6bd15e3bcc720ffa2bc4d6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710282"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="087ee-102">Después de eliminar (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="087ee-102">After Delete macro event</span></span>

<span data-ttu-id="087ee-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="087ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="087ee-104">El evento **Después de eliminar** se produce después de eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="087ee-104">The **After Delete** event occurs after a record is deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="087ee-105">[!NOTA] El evento **Después de eliminar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="087ee-105">The **After Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="087ee-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="087ee-106">Remarks</span></span>

<span data-ttu-id="087ee-p101">Utilice el evento **Después de eliminar** para realizar cualquier acción que desee que se produzca cuando se elimina un registro. **Después de eliminar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="087ee-p101">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted. Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="087ee-109">Cuando se produce el evento **Después de eliminar**, los valores contenidos en el registro eliminado siguen estando disponibles.</span><span class="sxs-lookup"><span data-stu-id="087ee-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="087ee-110">Es posible que desee utilizar un valor eliminado para aumentar o disminuir un total, crear una pista de auditoría o comparar con un valor existente en un argumento *WhereCondition* .</span><span class="sxs-lookup"><span data-stu-id="087ee-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="087ee-p103">Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo utilizar una instrucción If para determinar si se ha cambiado el campo PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="087ee-p103">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="087ee-113">Puede obtener acceso a un valor del registro eliminado mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="087ee-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="087ee-114">Por ejemplo, para tener acceso al valor del campo QuantityInStock en el registro eliminado, utilice la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="087ee-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="087ee-115">Cuando finaliza el evento **Después de eliminar**, se eliminan permanentemente los valores contenidos en el registro eliminado.</span><span class="sxs-lookup"><span data-stu-id="087ee-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="087ee-116">Pueden utilizar los siguientes comandos de macro en el evento **Después de eliminar** .</span><span class="sxs-lookup"><span data-stu-id="087ee-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="087ee-117">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="087ee-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="087ee-118">Comando</span><span class="sxs-lookup"><span data-stu-id="087ee-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="087ee-119">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="087ee-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="087ee-120"><a href="comment-macro-statement.md">Instrucción de macro de comentario</a></span><span class="sxs-lookup"><span data-stu-id="087ee-120"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-121">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="087ee-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="087ee-122"><a href="group-macro-statement.md">Instrucción de macro de grupo</a></span><span class="sxs-lookup"><span data-stu-id="087ee-122"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-123">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="087ee-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="087ee-124"><a href="if-then-else-macro-block.md">If... A continuación... Bloque de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="087ee-124"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-125">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="087ee-126"><a href="createrecord-data-block.md">Acción de macro CrearRegistro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-126"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-127">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="087ee-128"><a href="editrecord-data-block.md">Acción de macro EditarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-128"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-129">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="087ee-130"><a href="foreachrecord-data-block.md">Acción de macro ParaCadaRegistro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-130"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-131">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="087ee-132"><a href="lookuprecord-data-block.md">Bloque de datos BuscarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-132"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-133">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-134"><a href="cancelrecordchange-macro-action.md">Acción de macro CancelarCambioDeRegistro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-135">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-136"><a href="clearmacroerror-macro-action.md">Acción de macro BorrarErrorDeMacro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-136"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-137">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-138"><a href="deleterecord-macro-action.md">Acción de macro DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="087ee-138"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-139">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-140"><a href="exitforeachrecord-macro-action.md">Acción de macro Salirdecadaregistro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-141">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-142"><a href="logevent-macro-action.md">Acción de macro LogEvent</a></span><span class="sxs-lookup"><span data-stu-id="087ee-142"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-143">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-144"><a href="onerror-macro-action.md">Acción de macro AlOcurrirError</a></span><span class="sxs-lookup"><span data-stu-id="087ee-144"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-145">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-146"><a href="raiseerror-macro-action.md">Acción de macro Provocarerror</a></span><span class="sxs-lookup"><span data-stu-id="087ee-146"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-147">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-148"><a href="rundatamacro-macro-action.md">Acción de macro EjecutarMacroDeDatos</a></span><span class="sxs-lookup"><span data-stu-id="087ee-148"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-149">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-150"><a href="sendemail-macro-action.md">Acción de macro EnviarCorreoElectrónico</a></span><span class="sxs-lookup"><span data-stu-id="087ee-150"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-151">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-152"><a href="setfield-macro-action.md">Acción de macro SetField</a></span><span class="sxs-lookup"><span data-stu-id="087ee-152"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-153">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-154"><a href="setlocalvar-macro-action.md">Acción de macro EstablecerVariableLocal</a></span><span class="sxs-lookup"><span data-stu-id="087ee-154"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="087ee-155">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-156"><a href="stopallmacros-macro-action.md">Acción de macro DetenerTodasMacros</a></span><span class="sxs-lookup"><span data-stu-id="087ee-156"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="087ee-157">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="087ee-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="087ee-158"><a href="stopmacro-macro-action.md">Acción de macro DetenerMacro</a></span><span class="sxs-lookup"><span data-stu-id="087ee-158"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="087ee-159">Para crear una macro de datos que capture el evento **Después de eliminar**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="087ee-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="087ee-160">Abra la tabla en la que desee capturar el evento **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="087ee-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="087ee-161">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="087ee-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="087ee-162">Una macro de datos vacía se muestra en el Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="087ee-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="087ee-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="087ee-163">Example</span></span>

<span data-ttu-id="087ee-p104">En el ejemplo de código siguiente se utiliza el evento **Después de eliminar** para realizar algún procesamiento cuando se elimina un registro de la tabla Donativos. Cuando se elimina un registro, la cantidad del donativo se resta del campo DonativosRecibidos de la tabla DonativosRecibidos y del campo TotalDonado de la tabla Donantes.</span><span class="sxs-lookup"><span data-stu-id="087ee-p104">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="087ee-166">**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**</span><span class="sxs-lookup"><span data-stu-id="087ee-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="087ee-167">Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="087ee-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="087ee-168">Abra la tabla en la que desee capturar el evento **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="087ee-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="087ee-169">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="087ee-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="087ee-170">Seleccione el código que aparece debajo y a continuación, presione CTRL+C para copiarlo al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="087ee-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="087ee-171">Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="087ee-171">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterDelete"> 
        <Statements> 
          <Comment>Initialize a variable and assign the old</Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Old].[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Old].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Collapsed="true" Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Old].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
```

<br/>

```vb
    SetLocalVar 
                    Name    varAmount 
              Expression   =[Old].[Amount] 
     
    If   Not(IsNull([Old].[CampaignID]]))   Then 
     
         For Each Record In     Campaigns 
            Where Condition     =[ID]=[Old].[CampaignID] 
                      Alias 
            EditRecord 
                      Alias 
                  SetField   ([DonationsReceived], [DonationsReceived] - [varAmount]) 
            End EditRecord 
     
    End If 
     
    If   Not(IsNull([Old].[DonorID]]))   Then 
     
         For Each Record In    Donors 
            Where Condition     =[ID]=[Old].[DonorID] 
                      Alias 
            EditRecord 
                      Alias 
     
              SetField 
                             Name   [TotalDonated] 
                            Value   =[TotalDonated]-[varAmount] 
            End EditRecord 
    End If
```
