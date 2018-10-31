---
title: Acción de Macro eco (referencia de escritorio de la base de datos de Access)
TOCTitle: Echo Macro Action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39471ea4bab2ec1bbeb8cd22ecb00aa5df3bc411
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863972"
---
# <a name="echo-macro-action"></a>Acción de macro Echo


**Se aplica a**: Access 2013 | Office 2013

Puede usar la acción **Eco** para especificar si se activa el eco. Por ejemplo, puede usar esta acción para ocultar o mostrar los resultados de una macro mientras se ejecuta.

## <a name="setting"></a>Configuración


> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.



La acción **Eco** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Eco activo</strong></p></td>
<td><p>Haga clic en <strong>Sí</strong> (activar el eco) o <strong>No</strong> (desactivar el eco) en el cuadro <strong>Eco activo</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Sí</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Texto de la barra de estado</strong></p></td>
<td><p>El texto para mostrar en la barra de estado cuando el eco está desactivado. Por ejemplo, cuando se desactiva el eco, puede mostrar la barra de estado &quot;se está ejecutando la macro.&quot;</p></td>
</tr>
</tbody>
</table>


Cuando ejecuta una macro, la actualización de la pantalla suele mostrar la información no esencial para el funcionamiento de la macro. Al configurar el argumento **Eco activo** en **No**, la macro se ejecuta sin actualizar la pantalla. Cuando la macro termina, Access activa automáticamente el eco y vuelve a dibujar la pantalla. La configuración **No** para el argumento **Eco activo** no afecta a la funcionalidad de la macro o a sus resultados.

La acción **Eco** no suprime la visualización de los cuadros de diálogo modales, como mensajes de error o formularios emergentes, como hojas de propiedades. Puede usar los cuadros de diálogo y los formularios emergentes para recopilar o mostrar información, incluso si el eco está desactivado. Para suprimir todos los cuadros de diálogo o de mensaje, excepto los cuadros de mensaje de error y los cuadros de diálogo que necesitan que el usuario introduzca información, use la acción **EstablecerAdvertencias**.

Puede ejecutar la acción **Eco** varias veces en una macro. Esto permite cambiar el texto de la barra de estado mientras se ejecuta la macro.

Si desactiva el eco, puede usar la acción **MostrarCursorDeRelojDeArena** para cambiar el puntero del ratón por un icono de reloj de arena (o cualquier otro puntero del ratón que haya configurado en "Ocupado") para proporcionar una indicación visual de que la macro se está ejecutando.

Para ejecutar la acción **Eco** en un módulo Visual Basic para Aplicaciones (VBA), use el método **Eco** del objeto **DocMd**.

## <a name="examples"></a>Ejemplos

**Configurar el valor de un control con una macro**

La siguiente macro abre el formulario Agregar productos desde un botón del formulario Proveedores. Muestra el uso de las acciones **Eco**, **CerrarVentana**, **AbrirFormulario**, **ConfigurarValor** e **IrAControl**. La acción **ConfigurarValor** configura el control Id. de proveedor en el formulario Productos para el proveedor actual del formulario Proveedores. La acción **IrAControl** mueve el foco al campo Id. de categoría, donde puede empezar a introducir los datos para el nuevo producto. Esta macro se debe adjuntar al botón Agregar productos del formulario Proveedores.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Acción</p></th>
<th><p>Argumentos: Configuración</p></th>
<th><p>Comentario</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Eco</strong></p></td>
<td><p><strong>Eco activo</strong>: <strong>No</strong></p></td>
<td><p>Detener la actualización de la pantalla mientras se ejecuta la macro.</p></td>
</tr>
<tr class="even">
<td><p><strong>CerrarVentana</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>Nombre de FormObject</strong>: lista de producto <strong>Guardar</strong>: <strong>No</strong></p></td>
<td><p>Cerrar el formulario Lista de productos</p></td>
</tr>
<tr class="odd">
<td><p><strong>AbrirFormulario</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></p></td>
<td><p>Abrir el formulario Productos.</p></td>
</tr>
<tr class="even">
<td><p><strong>ConfigurarValor</strong></p></td>
<td><p><strong>Elemento</strong>: [Forms]![Products]![SupplierID] <strong>Expresión</strong>: IdProveedor</p></td>
<td><p>Configurar el control Id. de proveedor para el proveedor actual del formulario Proveedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IrAControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: IdCategoría</p></td>
<td><p>Ir al control Id. de categoría.</p></td>
</tr>
</tbody>
</table>


**Sincronizar los formularios con una macro**

La siguiente macro abre el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.

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
<td><p><strong>Eco</strong></p></td>
<td><p><strong>Eco activo</strong>: <strong>No</strong></p></td>
<td><p>Detener la actualización de la pantalla mientras se ejecuta la macro.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([Id. de proveedor])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos. <strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</p></td>
<td><p>Si no hay ningún proveedor actual en el formulario Proveedores, mostrar un mensaje.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>IrAControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: NombreDeEmpresa</p></td>
<td><p>Mover el foco al control NombreDeEmpresa.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>DetenerMacro</strong></p></td>
<td><p></p></td>
<td><p>Detener la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>AbrirFormulario</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre de DatasheetFilter</strong>: <strong>condición Where</strong>: [ID de proveedor] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></p></td>
<td><p>Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoverYCambiarTamañoDeVentana</strong></p></td>
<td><p><strong>Derecha</strong>: 0.7799&quot; <strong>hacia abajo</strong>: 1,8&quot;</p></td>
<td><p>Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</p></td>
</tr>
</tbody>
</table>

