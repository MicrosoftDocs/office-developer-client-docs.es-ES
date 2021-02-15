---
title: AlOcurrirError (acción de macro)
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288458"
---
# <a name="onerror-macro-action"></a>AlOcurrirError (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **AlOcurrirError** para especificar lo que va a ocurrir cuando se produce un error en una macro.

## <a name="setting"></a>Setting

La acción **AlOcurrirError** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Ve a </p></td>
<td><p>Permite especificar el comportamiento general que debe producirse cuando se detecta un error. Haga clic en la flecha desplegable y, a continuación, haga clic en uno de los siguientes valores:</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Next</strong></p></td>
<td><p>Microsoft Office Access 2007 registra los detalles del error en el objeto <strong>ErrorDeMacro</strong> pero no detiene la macro. La macro continúa con la siguiente acción.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre de macro</strong></p></td>
<td><p>Access detiene la macro actual y ejecuta la macro especificada en el argumento <strong>Nombre de macro</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Error</strong></p></td>
<td><p>Access detiene la macro actual y muestra un mensaje de error.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Macro Name</p></td>
<td><p>Si el argumento Ir a se establece en Nombre de macro, escriba el nombre de la macro que se usará para el tratamiento de errores. El nombre que escriba debe coincidir con un nombre de la <strong>columna Nombre de</strong> macro de la macro actual; no puede escribir el nombre de un objeto de macro diferente. En el ejemplo siguiente, la macro <strong>ErrorHandler</strong> está contenida en el mismo objeto de macro que la <strong>acción OnError.</strong> El valor de este argumento debe mantenerse en blanco si el argumento Ir a está establecido en <strong>Siguiente</strong> o en <strong>Error</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

- La acción **AlOcurrirError** suele situarse al comienzo de una macro, si bien se puede colocar también más adelante. Las reglas establecidas por la acción se harán efectivas cuando se ejecute la acción.

- Si se establece el argumento Ir a en **Error**, Access se comporta de la misma manera que se comportaría si no hubiera ninguna acción **AlOcurrirError** en la macro. Es decir, si se detecta un error, Access detiene la macro y muestra un mensaje de error estándar. El valor **Error** se usa principalmente para desactivar el tratamiento de errores establecido anteriormente en una macro.

## <a name="example"></a>Ejemplo

En la siguiente macro se muestra el uso de la acción **AlOcurrirError**. En este ejemplo, la acción **AlOcurrirError** especifica que Access ejecute una macro de tratamiento de errores personalizada denominada ErrorHandler cuando se produzca un error. Cuando se produce un error, se llama al submacro CatchErrors. Si el número de error es 2102, se muestra un mensaje específico y se detiene la ejecución de la macro. De lo contrario, se muestra un mensaje que describe el error y se pausa la macro para que pueda realizar una solución de problemas adicional. Esta macro mostrará un cuadro de mensaje referente al objeto **ErrorDeMacro** para mostrar información sobre el error.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
