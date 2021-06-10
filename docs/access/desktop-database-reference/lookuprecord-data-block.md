---
title: Bloque de datos LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734213"
---
# <a name="lookuprecord-data-block"></a>Bloque de datos LookupRecord

**Se aplica a:** Access 2013, Office 2013

Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico.

> [!NOTE]
> El bloque de datos **BuscarRegistro** solo está disponible en macros de datos.

## <a name="setting"></a>Configuración

La acción **EstablecerCampo** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Necesario</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Hacia dentro</p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que identifica el registro en el que se operará. El <em>argumento In</em> puede contener el nombre de la tabla, una consulta select o una instrucción SQL.</p><p><strong>NOTA:</strong>El registro especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Condición WHERE</p></td>
<td><p>No</p></td>
<td><p>Una expresión de cadena que se utiliza para restringir el intervalo de datos en el que se ejecuta el bloque de datos <strong>BuscarRegistro</strong>. Por ejemplo, los criterios suelen ser equivalentes a la cláusula WHERE en una SQL expresión, sin la palabra WHERE. Si se omiten criterios, el bloque de datos <strong>LookupRecord</strong> funciona en todo el dominio especificado por el <em>argumento In.</em> Cualquier campo que se incluya en los criterios debe ser también un campo del argumento <em>En</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>No</p></td>
<td><p>Cadena que proporciona un nombre alternativo para el registro especificado por el <em>argumento In.</em> Se utiliza a menudo para acortar el nombre de la tabla en referencias posteriores con el fin de evitar posibles referencias ambiguas. Si no se especifica ningún <em>Alias</em>, se utilizará el nombre de la tabla o consulta como el alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Si los criterios especificados por los argumentos *In* y *Where Condition* devuelven más de un registro, el bloque de datos **LookupRecord** solo funcionará en el primer registro.  En el caso de que ningún registro coincida con los criterios especificados, Access omitirá el conjunto de acciones contenidas en el bloque **LookupRecord,** como si hubiera sido una expresión de bloque de macro **[If](if-then-else-macro-block.md)** que se evaluó como false.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor de una macro de datos con nombre. Se devuelve una clase ReturnVar denominada **CurrentServiceRequest** a la subrutina Visual Basic para Aplicaciones (VBA) que llamó a la macro de datos con nombre.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

En el ejemplo siguiente se muestra cómo usar la acción RaiseError para cancelar el evento de macro de datos Before Change. Cuando se actualiza el campo AssignedTo, se usa un bloque de datos LookupRecord para determinar si el técnico asignado está asignado actualmente a una solicitud de servicio abierta. Si esto es así, el evento Before Change se cancela y el registro no se actualiza.

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
