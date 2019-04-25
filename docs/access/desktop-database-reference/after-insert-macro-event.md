---
title: Después de insertar (evento de macro)
TOCTitle: After Insert macro event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c84a737d08b791bfe560bfe6af6bcc59a14d2678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297224"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="c3bde-102">Después de insertar (evento de macro)</span><span class="sxs-lookup"><span data-stu-id="c3bde-102">After Insert macro event</span></span>

<span data-ttu-id="c3bde-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3bde-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3bde-104">El evento **Después de insertar** se produce después de agregar un registro.</span><span class="sxs-lookup"><span data-stu-id="c3bde-104">The **After Insert** event occurs after a record is added.</span></span>

> [!NOTE]
> <span data-ttu-id="c3bde-105">El evento **Después de insertar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="c3bde-105">The **After Insert** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3bde-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3bde-106">Remarks</span></span>

<span data-ttu-id="c3bde-p101">Utilice el evento **Después de insertar** para realizar cualquier acción que desee que se produzca cuando se agrega un registro a una tabla. **Después de insertar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="c3bde-p101">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table. Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="c3bde-109">Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c3bde-109">You can use the *Updated("**Field Name**")* function to determine whether a field has changed.</span></span> <span data-ttu-id="c3bde-110">En el ejemplo de código siguiente se muestra cómo utilizar una instrucción **If** para determinar si se ha cambiado el campo PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="c3bde-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="c3bde-111">La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Después de insertar**.</span><span class="sxs-lookup"><span data-stu-id="c3bde-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3bde-112">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="c3bde-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="c3bde-113">Comando</span><span class="sxs-lookup"><span data-stu-id="c3bde-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-114">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="c3bde-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="c3bde-115"><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-116">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="c3bde-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="c3bde-117"><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-118">Flujo de programas</span><span class="sxs-lookup"><span data-stu-id="c3bde-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="c3bde-119"><a href="if-then-else-macro-block.md">If...Then...Else (bloque de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-120">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c3bde-121"><a href="createrecord-data-block.md">CrearRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-121"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-122">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c3bde-123"><a href="editrecord-data-block.md">EditarRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-123"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-124">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c3bde-125"><a href="foreachrecord-data-block.md">ParaCadaRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-125"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-126">Bloque de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="c3bde-127"><a href="lookuprecord-data-block.md">BuscarRegistro (bloque de datos)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-128">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-129"><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-130">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-131"><a href="clearmacroerror-macro-action.md">BorrarErrorDeMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-132">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-133"><a href="deleterecord-macro-action.md">EliminarRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-134">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-135"><a href="exitforeachrecord-macro-action.md">SalirDeCadaRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-136">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-137"><a href="logevent-macro-action.md">RegistrarEvento (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-138">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-139"><a href="onerror-macro-action.md">AlOcurrirError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-140">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-141"><a href="raiseerror-macro-action.md">ProvocarError (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-142">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-143"><a href="rundatamacro-macro-action.md">EjecutarMacroDeDatos (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-144">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-145"><a href="sendemail-macro-action.md">EnviarCorreoElectrónico (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-146">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-147"><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-148">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-149"><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3bde-150">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-151"><a href="stopallmacros-macro-action.md">DetenerTodasMacros (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3bde-152">Acción de datos</span><span class="sxs-lookup"><span data-stu-id="c3bde-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="c3bde-153"><a href="stopmacro-macro-action.md">DetenerMacro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="c3bde-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3bde-154">Para crear una macro de datos que capture el evento **Después de insertar**, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c3bde-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="c3bde-155">Abra la tabla en la que desee capturar el evento **Después de insertar**.</span><span class="sxs-lookup"><span data-stu-id="c3bde-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="c3bde-156">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de insertar**.</span><span class="sxs-lookup"><span data-stu-id="c3bde-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="c3bde-157">Una macro de datos vacía se muestra en el Diseñador de macros.</span><span class="sxs-lookup"><span data-stu-id="c3bde-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="c3bde-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3bde-158">Example</span></span>

<span data-ttu-id="c3bde-p103">En el ejemplo de código siguiente se utiliza el evento **Después de insertar** para realizar algún procesamiento cuando se agrega un registro de la tabla Donativos. Cuando se agrega un registro, la cantidad del donativo se suma al campo DonativosRecibidos de la tabla Campañas y al campo TotalDonado de la tabla Donantes.</span><span class="sxs-lookup"><span data-stu-id="c3bde-p103">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="c3bde-161">**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**</span><span class="sxs-lookup"><span data-stu-id="c3bde-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="c3bde-162">Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c3bde-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="c3bde-163">Abra la tabla en la que desee capturar el evento **Después de insertar**.</span><span class="sxs-lookup"><span data-stu-id="c3bde-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="c3bde-164">En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de insertar**.</span><span class="sxs-lookup"><span data-stu-id="c3bde-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="c3bde-165">Seleccione el código en el siguiente ejemplo de código y, a continuación, presione CTRL+C para copiarlo al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c3bde-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="c3bde-166">Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="c3bde-166">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros> 
      <DataMacro Event="AfterInsert"> 
        <Statements> 
          <Comment>This data macro increments the DonationsReceived field in Campaigns and theAmountCollected field in Pledges </Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Donations].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]+[varAmount]</Argument> 
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
              <Condition>Not (IsNull([DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Donations].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]+[varAmount]</Argument> 
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
                  Name   varAmount 
            Expression   =[Amount] 
     
    If   Not (IsNull([CampaignID]))   Then 
     
         For Each Record In   Campaigns 
            Where Condition   =[ID]=[Donations].[CampaignID] 
                      Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [DonationsReceived] 
                                Value   =[DonationsReceived]+[varAmount] 
                End EditRecord 
    End If 
     
    If   Not (IsNull([DonorID]))   Then 
     
         For Each Record In  Donors 
            WhereCondition   =[ID]=[Donations].[DonorID] 
                     Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [TotalDonated] 
                                Value   =[TotalDonated]+[varAmount] 
                 End EditRecord 
    End If
```
