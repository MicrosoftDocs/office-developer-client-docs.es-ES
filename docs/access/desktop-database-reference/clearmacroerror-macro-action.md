---
title: BorrarErrorDeMacro (acción de macro)
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296377"
---
# <a name="clearmacroerror-macro-action"></a>BorrarErrorDeMacro (acción de macro)


**Se aplica a:** Access 2013, Office 2013


Puede usar la acción **BorrarErrorDeMacro** para borrar la información acerca de un error que está almacenado en el objeto **ErrorDeMacro**.

## <a name="setting"></a>Setting

La acción **BorrarErrorDeMacro** no tiene argumentos.

## <a name="remarks"></a>Comentarios

- Cuando se produce un error en una macro, se almacena información sobre el error en el objeto **ErrorDeMacro**. Si no ha usado la acción **[AlocurrirError](onerror-macro-action.md)** para suprimir mensajes de error, la macro se detiene y la información de error se muestra en un mensaje de error estándar. Sin embargo, si  ha usado la acción AlocurrirError para suprimir mensajes de error, es posible que desee usar la información almacenada en el objeto **MacroError** en una condición o en un mensaje de error personalizado.
    
  Una vez controlado un error, la información almacenada en el objeto **ErrorDeMacro** ya no está actualizada, por lo que se recomienda borrar el objeto mediante la acción **BorrarErrorDeMacro**. De este modo, se restablece en 0 el número de error almacenado en el objeto **ErrorDeMacro** y se borra cualquier otra información sobre el error que esté almacenada en el objeto, como la descripción del error, el nombre de la macro, el nombre de la acción, la condición y los argumentos. Esto permite volver a examinar más adelante el objeto **ErrorDeMacro** para comprobar si se ha producido otro error.

- El objeto **ErrorDeMacro** se borra automáticamente cuando finaliza cualquier macro, de modo que no necesita utilizar la acción **BorrarErrorDeMacro** al finalizar una macro.

- El objeto **ErrorDeMacro** contiene información referente a un solo error a la vez. Si se ha producido más de un error en una macro, el objeto **ErrorDeMacro** contiene solo la información sobre el último error.

- Para ejecutar la acción **BorrarErrorDeMacro** en un módulo de VBA, utilice el método **BorrarErrorDeMacro** del objeto **DoCmd**.

## <a name="example"></a>Ejemplo

En la siguiente macro se usa la acción **AlOcurrirError** con el argumento **Siguiente** para suprimir los mensajes de error y, a continuación, se usa la acción **AbrirFormulario** para abrir un formulario. Para este ejemplo, se crea deliberadamente un error usando la acción **IrARegistro** para ir al registro anterior. La condición **\[ MacroError \] . \[ El \] \< \> número 0** prueba el **objeto MacroError.** Si se genera un error, su número no es cero y se ejecuta la acción **CuadroDeMensaje**. En el cuadro de mensaje aparece el nombre de la acción que causó el error (en este caso, la acción **IrARegistro** ) y se muestra el número de error. Por último, al ejecutarse la acción **BorrarErrorDeMacro** se borra el objeto **ErrorDeMacro**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OnError</strong></p></td>
<td><p><strong>Ir a</strong>: <strong>Siguiente</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: Vista<strong>CategoryForm</strong>: <strong>Modo FormWindow</strong>: <strong>Normal</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</p></td>
</tr>
<tr class="even">
<td><p>[MacroError]. [Número] &lt; &gt; 0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: = &quot; Error # &quot; &amp; [ErrorDeMacro].[ Number] &amp; &quot; on &quot; &amp; [MacroError].[ Acción &amp; &quot; ActionName]. &quot; <strong>Sonido</strong>: <strong>YesType</strong>: Información</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

