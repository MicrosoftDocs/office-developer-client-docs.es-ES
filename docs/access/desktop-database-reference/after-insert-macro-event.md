---
title: Después de insertar (evento de macro)
TOCTitle: After Insert Macro Event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 171c7b11db6fa79c6b69f3517abaddf052c96da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880729"
---
# <a name="after-insert-macro-event"></a>Después de insertar (evento de macro)


**Se aplica a**: Access 2013, Office 2013

El evento **Después de insertar** se produce después de agregar un registro.


> [!NOTE]
> [!NOTA] El evento **Después de insertar** solo está disponible en macros de datos.



## <a name="remarks"></a>Comentarios

Utilice el evento **Después de insertar** para realizar cualquier acción que desee que se produzca cuando se agrega un registro a una tabla. **Después de insertar** se suele utilizar para exigir reglas de negocio, flujos de trabajo, actualizar un total agregado y enviar notificaciones.

Puede utilizar la función **Updated("*Nombre del campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo utilizar una instrucción **If** para determinar si se ha cambiado el campo PaidInFull.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Después de insertar**.

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


Para crear una macro de datos que capture el evento **Después de insertar**, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Después de insertar**.

2.  En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de insertar**.

Una macro de datos vacía se muestra en el Diseñador de macros.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se utiliza el evento **Después de insertar** para realizar algún procesamiento cuando se agrega un registro de la tabla Donativos. Cuando se agrega un registro, la cantidad del donativo se suma al campo DonativosRecibidos de la tabla Campañas y al campo TotalDonado de la tabla Donantes.

**Haga clic aquí para ver una copia de la macro que puede pegar en el Diseñador de macros.**

Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Después de insertar**.

2.  En la ficha **Tabla**, en el grupo **Eventos posteriores**, haga clic en **Después de insertar**.

3.  Seleccione el código en el siguiente ejemplo de código y, a continuación, presione CTRL+C para copiarlo al Portapapeles.

4.  Active la ventana del Diseñador de macros y, a continuación, presione CTRL+V.

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
