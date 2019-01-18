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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703961"
---
# <a name="before-change-macro-event"></a>Cambio previo (evento de macro)

**Se aplica a**: Access 2013, Office 2013

El evento **Cambio previo** se produce cuando cambia un registro, pero antes de confirmar el cambio.

> [!NOTE]
> [!NOTA] El evento **Cambio previo** solo está disponible en macros de datos.

## <a name="remarks"></a>Comentarios

Utilice el evento **Cambio previo** para realizar cualquier acción que desee que ocurra antes de cambiar un registro. **Cambio previo** se suele utilizar para realizar la validación y para provocar mensajes de error personalizados.

Puede usar la función **Updated ("*Nombre de campo*")** para determinar si un campo ha cambiado. En el ejemplo de código siguiente se muestra cómo usar una instrucción **If** para determinar si se ha cambiado el campo PaidInFull.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Utilice la propiedad **EsInsertar** para determinar si el evento **Cambio previo** se desencadenó por la creación de un nuevo registro o por un cambio en un registro existente. La propiedad **EsInsertar** contiene **Verdadero** si el evento se desencadenó por un nuevo registro y **Falso** si el evento se desencadenó por un cambio en un registro existente.

En el ejemplo de código siguiente se muestra la sintaxis para utilizar la propiedad **EsInsertar**.

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

Puede obtener acceso al valor anterior de un campo mediante la sintaxis siguiente.

```vb
    [Old].[Field Name]
```

Por ejemplo, para tener acceso al valor anterior del campo QuantityInStock, utilice la sintaxis siguiente.

```vb
    [Old].[QuantityInStock]
```

Los valores anteriores se eliminan permanentemente cuando finaliza el evento **Cambio previo**.

Puede cancelar el evento **Cambio previo** mediante la acción **ProvocarError**. Cuando se provoca un error se descartan los cambios incluidos en el evento **Cambio previo**.

La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Cambio previo**.

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
<td><p><a href="comment-macro-statement.md">Instrucción de macro de comentario</a></p></td>
</tr>
<tr class="even">
<td><p>Flujo de programas</p></td>
<td><p><a href="group-macro-statement.md">Instrucción de macro de grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Flujo de programas</p></td>
<td><p><a href="if-then-else-macro-block.md">If... A continuación... Bloque de macro Else</a></p></td>
</tr>
<tr class="even">
<td><p>Bloque de datos</p></td>
<td><p><a href="lookuprecord-data-block.md">Acción de macro BuscarRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Acción de macro BorrarErrorDeMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="onerror-macro-action.md">Acción de macro AlOcurrirError</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="raiseerror-macro-action.md">Acción de macro Provocarerror</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="setfield-macro-action.md">Acción de macro SetField</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="setlocalvar-macro-action.md">Acción de macro EstablecerVariableLocal</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="stopmacro-macro-action.md">Acción de macro DetenerMacro</a></p></td>
</tr>
</tbody>
</table>


Para crear una macro de datos que capture el evento **Cambio previo**, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Cambio previo**.

2.  En la ficha **Tabla**, en el grupo **Eventos anteriores**, haga clic en **Cambio previo**.

Una macro de datos vacía se muestra en el Diseñador de macros.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se usa el evento **Cambio previo** para validar los campos de estado. Se produce un error si el campo Resolución contiene un valor inadecuado.

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

Para ver este ejemplo en el Diseñador de macros, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Cambio previo**.

2.  En la ficha **Tabla**, en el grupo **Eventos anteriores**, haga clic en **Cambio previo**.

3.  Seleccione el código en el siguiente ejemplo de código y, a continuación, presione **CTRL+c** para copiarlo en el Portapapeles.

4.  Activar la ventana del Diseñador de macros y, a continuación, presione **CTRL+v**.



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

En el ejemplo siguiente se muestra cómo usar la acción Provocarerror para cancelar el evento de macro de datos antes de cambiar. Cuando se actualiza el campo AssignedTo, un bloque de datos BuscarRegistro se usa para determinar si el técnico asignado actualmente está asignado a una solicitud de servicio abiertas. Si es true, a continuación, se cancela el evento cambio previo y no se actualiza el registro.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
