---
title: CancelarEvento (acción de macro)
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7999d2acd19fd1f6aa4d7dd9dccd88b7ffea88a7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925333"
---
# <a name="cancelevent-macro-action"></a>CancelarEvento (acción de macro)


**Se aplica a**: Access 2013, Office 2013


Puede usar la acción **CancelarEvento** para cancelar el evento que causó que Access ejecutar la macro que contiene esta acción. El nombre de la macro es el valor de una propiedad de evento como **BeforeUpdate**, **OnOpen**, **OnUnload** u **OnPrint**.

## <a name="setting"></a>Configuración

La acción **CancelarEvento** no tiene argumentos.

## <a name="remarks"></a>Comentarios

En un formulario, suele utilizarse la acción **CancelarEvento** en una macro de validación con la propiedad de evento **BeforeUpdate**. Cuando un usuario escribe datos en un control o en un registro, Access ejecuta la macro antes de agregar los datos a la base de datos. Si los datos no pasan las condiciones de validación de la macro, la acción **CancelarEvento** cancela el proceso de actualización antes de que se inicie.

A menudo, esta acción se usa con la acción **CuadroDeMensaje** para indicar que los datos no han pasado las condiciones de validación y para proporcionar información útil sobre la clase de datos que debe especificarse.

La acción **CancelarEvento** puede cancelar los eventos siguientes.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Dirty</strong></p></td>
<td><p><strong>MouseDown</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeDelConfirm</strong></p></td>
<td><p><strong>Salir</strong></p></td>
<td><p><strong>NoData</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>BeforeInsert</strong></p></td>
<td><p><strong>Filter</strong></p></td>
<td><p><strong>Open</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Formato</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Delete</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!NOTA] Puede usar la acción **CancelarEvento** con el evento **BajarMouse** sólo para cancelar el evento que se produce al hacer clic con el botón secundario en un objeto.

Si la configuración de la propiedad de evento **AlHacerDobleClic** de un control especifica una macro que contiene la acción **CancelarEvento**, la acción cancela el evento **HacerDobleClic**.

Para los eventos que pueden cancelarse, el comportamiento predeterminado para el evento (es decir, lo que generalmente hace Access cuando ocurre un evento) se produce después de que se ejecuta la macro para el evento. Esto permite cancelar el comportamiento predeterminado. Por ejemplo, cuando hace doble clic en una palabra en la que está el punto de inserción en un cuadro de texto, Access en general selecciona la palabra. Puede cancelar este comportamiento predeterminado en una macro para el evento **HacerDobleClic** y realizar alguna otra acción, como abrir un formulario que contenga información acerca de los datos en el cuadro de texto. Para eventos que se pueden cancelar, el comportamiento predeterminado se produce antes de que se ejecuta la macro.

> [!NOTE]
> [!NOTA] Si la propiedad de evento **AlDescargar** de un formulario especifica una macro que lleva a cabo la acción **CancelarEvento**, no podrá cerrar el formulario. Debe corregir la condición que generó la acción **CancelarEvento** o abrir la macro y eliminar la acción **CancelarEvento**. Si el formulario es modal, no podrá abrir la macro.

Para llevar a cabo la acción **CancelarEvento** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **CancelEvent** del objeto **DoCmd**.

## <a name="example"></a>Ejemplo

 Validar datos con una macro

La siguiente macro de validación comprueba los códigos postales especificados en un formulario Proveedores. Muestra el uso de las acciones **DetenerMacro**, **CuadroDeMensaje**, **CancelarEvento** y **IrAControl**. Una expresión condicional comprueba el país o la región y el código postal especificados en un registro del formulario. Si el código postal no tiene el formato correcto para el país o la región, la macro muestra un cuadro de mensaje y cancela el proceso de guardar el registro. Después, lleva al usuario hasta el control CódigoPostal, donde puede corregir el error. Esta macro debe asociarse a la propiedad **AntesDeActualizar** del formulario Proveedores.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condición</p></th>
<th><p>Acción</p></th>
<th><p>Argumentos: Configuración</p></th>
<th><p>Comentario</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull([PaísRegión])</p></td>
<td><p>StopMacro</p></td>
<td><p></p></td>
<td><p>Si PaísRegión es <strong>Nulo</strong>, no se podrá validar el código postal.</p></td>
</tr>
<tr class="even">
<td><p>[PaísRegión] En (&quot;Francia&quot;,&quot;Italia&quot;,&quot;España&quot;) y longitud ([CódigoPostal]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>Mensaje: el código postal debe tener 5 caracteres. 

 Bip: <strong>Sí</strong> tipo: <strong>información</strong> título: Error de código Postal</p></td>
<td><p>Si el código postal no tiene 5 caracteres, mostrar un mensaje.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelarEvento</p></td>
<td><p></p></td>
<td><p>Cancelar el evento.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Nombre del control: CódigoPostal</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[PaísRegión] En (&quot;Australia&quot;,&quot;Singapur&quot;) y longitud ([CódigoPostal]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>Mensaje: el código postal debe tener 4 caracteres. 

 Bip: <strong>Sí</strong> tipo: <strong>información</strong> título: Error de código Postal</p></td>
<td><p>Si el código postal no tiene 4 caracteres, mostrar un mensaje.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>CancelarEvento</p></td>
<td><p></p></td>
<td><p>Cancelar el evento.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Nombre del control: CódigoPostal</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([PaísRegión] = &quot;Canadá&quot;) Y ([CódigoPostal] no le gusta&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;)</p></td>
<td><p>MessageBox</p></td>
<td><p>Mensaje: El código postal no es válido. Ejemplo de código de Canadá: H1J 1C3 Bip: <strong>Sí</strong> tipo: <strong>información</strong> título: Error de código Postal</p></td>
<td><p>Si el código postal no es correcto para Canadá, mostrar un mensaje. (Ejemplo de código canadiense: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelarEvento</p></td>
<td><p></p></td>
<td><p>Cancelar el evento.</p></td>
</tr>
</tbody>
</table>

