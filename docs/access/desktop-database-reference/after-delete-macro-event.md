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
# <a name="after-delete-macro-event"></a>Después de eliminar (evento de macro)


**Se aplica a**: Access 2013 | Office 2013

El evento **Después de eliminar** se produce después de eliminar un registro.


> [!NOTE]
> [!NOTA] El evento **Después de eliminar** solo está disponible en macros de datos.



## <a name="remarks"></a>Comentarios

Utilice el evento **Después de eliminar** para realizar cualquier acción que desee que se produzca cuando se elimina un registro. **Después de eliminar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.

Cuando se produce el evento **Después de eliminar**, los valores contenidos en el registro eliminado siguen estando disponibles. Es posible que desee utilizar un valor eliminado para aumentar o disminuir un total, crear una pista de auditoría o comparar con un valor existente en un argumento *WhereCondition* .

Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo utilizar una instrucción If para determinar si se ha cambiado el campo PaidInFull.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Puede obtener acceso a un valor del registro eliminado mediante la sintaxis siguiente.

`[Old].[Field Name]`

Por ejemplo, para tener acceso al valor del campo QuantityInStock en el registro eliminado, utilice la sintaxis siguiente.

`[Old].[QuantityInStock]`

Cuando finaliza el evento **Después de eliminar**, se eliminan permanentemente los valores contenidos en el registro eliminado.

Pueden utilizar los siguientes comandos de macro en el evento **Después de eliminar** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de comando</p></th>
<th><p>Comando</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Flujo de programas</p></td>
<td><p><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Flujo de programas</p></td>
<td><p><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Flujo de programas</p></td>
<td><p><a href="if-then-else-macro-block.md">Si...Entonces...Sino (bloque de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Bloque de datos</p></td>
<td><p><a href="createrecord-data-block.md">CrearRegistro (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloque de datos</p></td>
<td><p><a href="editrecord-data-block.md">EditarRegistro (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Bloque de datos</p></td>
<td><p><a href="foreachrecord-data-block.md">ParaCadaRegistro (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloque de datos</p></td>
<td><p><a href="lookuprecord-data-block.md">BuscarRegistro (bloque de datos)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="clearmacroerror-macro-action.md">BorrarErrorDeMacro (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="deleterecord-macro-action.md">EliminarRegistro (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">SalirDeCadaRegistro (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="logevent-macro-action.md">RegistrarEvento (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="onerror-macro-action.md">AlOcurrirError (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="raiseerror-macro-action.md">ProvocarError (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="rundatamacro-macro-action.md">EjecutarMacroDeDatos (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="sendemail-macro-action.md">EnviarCorreoElectrónico (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="stopallmacros-macro-action.md">DetenerTodasMacros (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="stopmacro-macro-action.md">DetenerMacro (acción de macro)</a></p></td>
</tr>
</tbody>
</table>


Para crear una macro de datos que capture el evento **Después de eliminar**, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Después de eliminar**.

2.  En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de eliminar**.

Una macro de datos vacía se muestra en el Diseñador de macros.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se utiliza el evento **Después de eliminar** para realizar algún procesamiento cuando se elimina un registro de la tabla Donativos. Cuando se elimina un registro, la cantidad del donativo se resta del campo DonativosRecibidos de la tabla DonativosRecibidos y del campo TotalDonado de la tabla Donantes.

**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**

Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Después de eliminar**.

2.  En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de eliminar**.

3.  Seleccione el código que aparece debajo y a continuación, presione CTRL+C para copiarlo al Portapapeles.

4.  Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.

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
