---
title: Acción de Macro SetReturnVar
TOCTitle: SetReturnVar Macro Action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a0c4d47283b059a32fa4df3ba8e1278c1fdcd17a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873988"
---
# <a name="setreturnvar-macro-action"></a>Acción de Macro SetReturnVar

**Se aplica a**: Access 2013, Office 2013

La acción **SetReturnVar** crea una variable de retorno y establece en un valor específico.

> [!NOTE]
> La acción **SetReturnVar** sólo está disponible en Macros de datos.

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
<th><p>Argumento</p></th>
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
<td><p>Expresión</p></td>
<td><p>Sí</p></td>
<td><p>Una expresión que se usará para establecer el valor de esta variable temporal. Delante de la expresión con el signo igual (=). Puede hacer clic en el botón <strong>Generar</strong> para usar el <strong>Generador de expresiones</strong> para definir este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La acción **SetReturnVar** se usa para crear un **ReturnVar**, que es la variable que se puede utilizar las macros que llaman a una macro de datos mediante el uso de la acción **EjecutarMacroDeDatos** .

Una vez creada una **ReturnVar** por la acción **SetReturnVar** , la macro llamada puede usar en una expresión. Por ejemplo, si ha creado un **ReturnVar** denominado **UpdateSuccess**, podría usar la variable utilizando la sintaxis siguiente:

```vb
    =[ReturnVars]![UpdateSuccess]
```

La acción **SetReturnVar** se puede usar en macros de datos con nombre. No está disponible en macros de datos que están asociadas a un evento de macro de datos.

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
