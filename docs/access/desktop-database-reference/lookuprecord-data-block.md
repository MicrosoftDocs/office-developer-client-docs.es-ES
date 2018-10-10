---
title: BuscarRegistro (bloque de datos)
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd0db6e818ab79fc124760509d07d60b954d49e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485413"
---
# <a name="lookuprecord-data-block"></a>BuscarRegistro (bloque de datos)

**Se aplica a**: Access 2013 | Office 2013

Un bloque de datos **BuscarRegistro** realiza un conjunto de acciones en un registro específico.

> [!NOTE]
> [!NOTA] El bloque de datos **BuscarRegistro** solo está disponible en macros de datos.

## <a name="setting"></a>Valores

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
<th><p>Obligatorio</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>In</p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que identifica el registro para funcionar en. El argumento <em>en</em> puede contener el nombre de la tabla, una consulta de selección o una instrucción SQL.</p>

> [!NOTE]
> El registro especificado no puede incluir datos almacenados en una tabla vinculada u origen de datos ODBC .


<p></p></td>
</tr>
<tr class="even">
<td><p>Condición WHERE</p></td>
<td><p>No</p></td>
<td><p>Expresión de cadena utilizada para restringir el intervalo de datos en la que el bloque de datos <strong>BuscarRegistro</strong> se lleva a cabo. Por ejemplo, criterios suelen ser equivalentes a la cláusula WHERE en una expresión SQL, sin la palabra donde. Si se omiten criterios, el bloque de datos <strong>BuscarRegistro</strong> funciona en todo el dominio especificado por el argumento <em>en</em> . Cualquier campo que se incluya en criterios debe ser también un campo de <em>en</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>No</p></td>
<td><p>Una cadena que proporciona un nombre alternativo para el registro especificado por el argumento <em>en</em> . A menudo se usa para acortar el nombre de tabla para las referencias subsiguientes a fin de evitar posibles referencias ambiguas. Si no se especifica ningún <em>Alias</em>, se utilizará el nombre de la tabla o consulta como el alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Si los criterios especificados por los argumentos *en* y *Condición Where* especifica más de un registro, el bloque de datos **BuscarRegistro** funcionará sólo en el primer registro.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor desde una macro de datos con nombre. Un ReturnVar denominado **CurrentServiceRequest** se devuelve a la macro o Visual Basic para la subrutina de aplicaciones (VBA) que llama a la macro de datos con nombre.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

En el ejemplo siguiente se muestra cómo usar la acción Provocarerror para cancelar el evento de macro de datos antes de cambiar. Cuando se actualiza el campo AssignedTo, un bloque de datos BuscarRegistro se usa para determinar si el técnico asignado actualmente está asignado a una solicitud de servicio abiertas. Si es true, se cancela el evento cambio previo y no se actualiza el registro.

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
