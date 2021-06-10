---
title: CuadroDeMensajes (acción de macro)
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1175e3903e54fd3420be43dfd9e3652d9990468b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289159"
---
# <a name="messagebox-macro-action"></a>CuadroDeMensajes (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **CuadroDeMensajes** para mostrar un cuadro de mensaje que contenga una advertencia o un mensaje informativo. Por ejemplo, puede usar la acción **CuadroDeMensajes** con macros de validación. Cuando un control o un registro produce un error en una condición de validación de la macro, un cuadro de mensaje puede mostrar un mensaje de error y proporcionar instrucciones sobre el tipo de datos que se debe introducir.

## <a name="setting"></a>Configuración

La acción **CuadroDeMensajes** tiene los siguientes argumentos.

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
<td><p><strong>Mensaje</strong></p></td>
<td><p>El texto del mensaje de texto. Introduzca el texto del mensaje en el cuadro <strong>Mensaje</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Puede escribir hasta 255 caracteres o introducir una expresión (precedida de un signo de igual).  </p></td>
</tr>
<tr class="even">
<td><p><strong>Sonido</strong></p></td>
<td><p>Especifica si el altavoz del equipo emite un sonido al mostrar el mensaje. Haga clic en <strong>Sí</strong> (emitir el sonido) o <strong>No</strong> (no emitir el sonido). El valor predeterminado es <strong>Sí</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Tipo</strong></p></td>
<td><p>El tipo de cuadro de mensaje. Cada tipo tiene un icono distinto. Haga clic en <strong>Ninguno</strong>, <strong>Crítico</strong>, <strong>¿Advertencia?</strong>, <strong>Advertencia</strong> o <strong>Información</strong>. El valor predeterminado es <strong>Ninguno</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Título</strong></p></td>
<td><p>El texto que se muestra en la barra de título del cuadro de mensaje. Por ejemplo, puede hacer que la barra de título muestre &quot; Validación de id. de cliente &quot; . Si deja este argumento en blanco, &quot; se muestra Microsoft &quot; Access.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar la acción **CuadroDeMensajes** para crear un mensaje de error con formato parecido a los mensajes de error integrados que muestra Microsoft Access. La acción **CuadroDeMensajes** permite proporcionar un mensaje en tres secciones para el argumento Mensaje. Las secciones se separan mediante el carácter "@".

En el siguiente ejemplo se muestra un cuadro de mensaje con formato con un mensaje con secciones. La primera sección del texto del mensaje se muestra como encabezado en negrita. La segunda sección se muestra como texto normal bajo el encabezado. La tercera sección se muestra como texto normal bajo la segunda sección, con una línea en blanco entre ellas.

Escriba la siguiente cadena en el argumento **Mensaje**:

**El botón \! @This no se work.@Try otro.**

No puede ejecutar la acción **CuadroDeMensajes** en un módulo Visual Basic para aplicaciones (VBA). En su lugar, use la función **CuadroMsj**.

## <a name="examples"></a>Ejemplos

**Sincronizar formularios con una macro**

La siguiente macro abre Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.

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
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Eco activo</strong>: <strong>No</strong></p></td>
<td><p>Detener la actualización de la pantalla mientras se ejecuta la macro.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: Mueva al registro de proveedores los productos que quiera ver y haga clic en el botón Revisar productos de nuevo. <strong>Pitido</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</p></td>
<td><p>Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: NombreDeEmpresa</p></td>
<td><p>Mover el foco al control NombreDeEmpresa.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Detener la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nombre del</strong>formulario : Vista lista <strong>de productos</strong>: <strong>DatasheetFilter Name</strong>: Where <strong>Condition</strong>: [SupplierID] = [Forms]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo De solo lecturaWindow</strong>: <strong>Normal</strong></p></td>
<td><p>Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Right</strong>: 0.7799 &quot; <strong>Down</strong>: 1.8&quot;</p></td>
<td><p>Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</p></td>
</tr>
</tbody>
</table>


**Validar los datos con una macro**

La siguiente macro de validación comprueba los códigos postales introducidos en el formulario Proveedores. Muestra el uso de las acciones **DetenerMacro**, **CuadroDeMensajes**, **CancelarEvento** e **IrAControl**. Una expresión condicional comprueba el país o región, y el código postal introducidos en un registro del formulario. Si el código postal no tiene el formato correcto para el país o región, la macro muestra un cuadro de mensaje y cancela el guardado del registro. Luego, devuelve el control CódigoPostal, donde puede corregir el error. Esta macro se debe adjuntar a la propiedad **BeforeUpdate** del formulario Proveedores.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Si PaísRegión es <strong>Null</strong>, el código postal no se podrá validar.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In ( &quot; France , Italy , Spain ) and &quot; &quot; &quot; &quot; &quot; Len([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: el código postal debe ser de 5 caracteres. <strong>Pitido</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Error de código postal</p></td>
<td><p>Si el código postal no tiene 5 caracteres, mostrar un mensaje.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancelar el evento.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: CódigoPostal</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In ( &quot; Australia , Singapore ) And &quot; &quot; &quot; Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: el código postal debe ser de 4 caracteres. <strong>Pitido</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Error de código postal</p></td>
<td><p>Si el código postal no tiene 4 caracteres, mostrar un mensaje.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancelar el evento.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: CódigoPostal</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Canada &quot; ) And ([PostalCode] Not Like &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: El código postal no es válido. Ejemplo de código canadiense: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Si el código postal no es correcto para Canadá, mostrar un mensaje. (Ejemplo de código canadiense: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancelar el evento.</p></td>
</tr>
</tbody>
</table>

