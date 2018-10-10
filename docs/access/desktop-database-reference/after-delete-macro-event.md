---
title: Después de eliminar (evento de macro)
TOCTitle: After Delete Macro Event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e803ccc915a939878cf758698a98661c2a3f5283
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484572"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="b077f-102">Después de eliminar (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="b077f-102">After Delete Macro Event</span></span>


<span data-ttu-id="b077f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b077f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b077f-104">El evento **Después de eliminar** se produce después de eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="b077f-104">The **After Delete** event occurs after a record is deleted.</span></span>


> [!NOTE]
> <span data-ttu-id="b077f-105">[!NOTA] El evento **Después de eliminar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="b077f-105">The **After Delete** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="b077f-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b077f-106">Remarks</span></span>

<span data-ttu-id="b077f-p101">Utilice el evento **Después de eliminar** para realizar cualquier acción que desee que se produzca cuando se elimina un registro. **Después de eliminar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b077f-p101">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted. Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="b077f-109">Cuando se produce el evento **Después de eliminar**, los valores contenidos en el registro eliminado siguen estando disponibles.</span><span class="sxs-lookup"><span data-stu-id="b077f-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="b077f-110">Es posible que desee utilizar un valor eliminado para aumentar o disminuir un total, crear una pista de auditoría o comparar con un valor existente en un argumento *WhereCondition* .</span><span class="sxs-lookup"><span data-stu-id="b077f-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="b077f-p103">Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo utilizar una instrucción If para determinar si se ha cambiado el campo PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="b077f-p103">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="b077f-113">Puede obtener acceso a un valor del registro eliminado mediante la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="b077f-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="b077f-114">Por ejemplo, para tener acceso al valor del campo QuantityInStock en el registro eliminado, utilice la sintaxis siguiente.</span><span class="sxs-lookup"><span data-stu-id="b077f-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="b077f-115">Cuando finaliza el evento **Después de eliminar**, se eliminan permanentemente los valores contenidos en el registro eliminado.</span><span class="sxs-lookup"><span data-stu-id="b077f-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="b077f-116">Pueden utilizar los siguientes comandos de macro en el evento **Después de eliminar** .</span><span class="sxs-lookup"><span data-stu-id="b077f-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b077f-117">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="b077f-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="b077f-118">Comando</span><span class="sxs-lookup"><span data-stu-id="b077f-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b077f-119">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="b077f-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="b077f-120"><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-120"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-121">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="b077f-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="b077f-122"><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-122"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-123">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="b077f-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="b077f-124"><a href="if-then-else-macro-block.md">Si...Entonces...Sino (bloque de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-124"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-125">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="b077f-126"><a href="createrecord-data-block.md">CrearRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-126"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-127">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="b077f-128"><a href="editrecord-data-block.md">EditarRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-128"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-129">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="b077f-130"><a href="foreachrecord-data-block.md">ParaCadaRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-130"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-131">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="b077f-132"><a href="lookuprecord-data-block.md">BuscarRegistro (bloque de datos)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-132"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-133">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-134"><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-135">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-136"><a href="clearmacroerror-macro-action.md">BorrarErrorDeMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-136"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-137">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-138"><a href="deleterecord-macro-action.md">EliminarRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-138"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-139">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-140"><a href="exitforeachrecord-macro-action.md">SalirDeCadaRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-141">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-142"><a href="logevent-macro-action.md">RegistrarEvento (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-142"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-143">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-144"><a href="onerror-macro-action.md">AlOcurrirError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-144"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-145">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-146"><a href="raiseerror-macro-action.md">ProvocarError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-146"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-147">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-148"><a href="rundatamacro-macro-action.md">EjecutarMacroDeDatos (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-148"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-149">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-150"><a href="sendemail-macro-action.md">EnviarCorreoElectrónico (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-150"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-151">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-152"><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-152"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-153">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-154"><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-154"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b077f-155">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-156"><a href="stopallmacros-macro-action.md">DetenerTodasMacros (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-156"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b077f-157">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="b077f-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="b077f-158"><a href="stopmacro-macro-action.md">DetenerMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b077f-158"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b077f-159">Para crear una macro de datos que capture el evento **Después de eliminar**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b077f-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="b077f-160">Abra la tabla en la que desee capturar el evento **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b077f-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="b077f-161">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b077f-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="b077f-162">Una macro de datos vacía se muestra en el Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="b077f-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="b077f-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b077f-163">Example</span></span>

<span data-ttu-id="b077f-p104">En el ejemplo de código siguiente se utiliza el evento **Después de eliminar** para realizar algún procesamiento cuando se elimina un registro de la tabla Donativos. Cuando se elimina un registro, la cantidad del donativo se resta del campo DonativosRecibidos de la tabla DonativosRecibidos y del campo TotalDonado de la tabla Donantes.</span><span class="sxs-lookup"><span data-stu-id="b077f-p104">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="b077f-166">**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**</span><span class="sxs-lookup"><span data-stu-id="b077f-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="b077f-167">Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b077f-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="b077f-168">Abra la tabla en la que desee capturar el evento **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b077f-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="b077f-169">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de eliminar**.</span><span class="sxs-lookup"><span data-stu-id="b077f-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="b077f-170">Seleccione el código que aparece debajo y a continuación, presione CTRL+C para copiarlo al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="b077f-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="b077f-171">Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="b077f-171">Activate the macro designer window and then press CTRL+V.</span></span>

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
