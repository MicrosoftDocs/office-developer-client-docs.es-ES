---
title: EstablecerVariableDevuelta (acción de macro)
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308676"
---
# <a name="setreturnvar-macro-action"></a>EstablecerVariableDevuelta (acción de macro)

**Se aplica a:** Access 2013, Office 2013

La acción **SetReturnVar** crea una variable de retorno y la establece en un valor específico.

> [!NOTE]
> La acción **SetReturnVar** solo está disponible en macros de datos.

## <a name="setting"></a>Configuración

La acción **SetReturnVar** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatorio</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nombre</p></td>
<td><p>Sí</p></td>
<td><p>Una cadena que especifica el nombre de la variable.</p></td>
</tr>
<tr class="even">
<td><p>Numérico</p></td>
<td><p>Sí</p></td>
<td><p>Una expresión que se utilizará para establecer el valor de esta variable temporal. No anteponga el signo igual (=) a la expresión. Puede hacer clic en el botón <strong>generar</strong> para usar el <strong>generador de expresiones</strong> para establecer este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **SetReturnVar** se usa para crear una **ReturnVar**, que es una variable que pueden usar las macros que llaman a una macro de datos mediante la acción **RunDataMacro** .

Una vez que la acción **SetReturnVar** crea **ReturnVar** , la macro de llamada puede usarla en una expresión. Por ejemplo, si ha creado un **ReturnVar** con el nombre **UpdateSuccess**, puede usar la variable mediante la siguiente sintaxis:

```vb
    =[ReturnVars]![UpdateSuccess]
```

La acción **SetReturnVar** sólo se puede usar en macros de datos con nombre. No está disponible en macros de datos que estén adjuntas a un evento de macro de datos.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar la acción SetReturnVar para devolver un valor de una macro de datos con nombre. Un ReturnVar denominado **CurrentServiceRequest** se devuelve a la subrutina o a la subrutina de Visual Basic para aplicaciones (VBA) que llama a la macro de datos con nombre.

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
