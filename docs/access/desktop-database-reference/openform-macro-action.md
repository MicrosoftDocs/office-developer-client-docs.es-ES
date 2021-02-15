---
title: AbrirFormulario (acción de macro)
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288374"
---
# <a name="openform-macro-action"></a>AbrirFormulario (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **AbrirFormulario** para abrir un formulario en la vista Formulario, Diseño, Vista preliminar u Hoja de datos. Puede seleccionar los modos de entrada de datos y ventana para el formulario y restringir los registros que se muestra en él.

## <a name="setting"></a>Setting

La acción **AbrirFormulario** incluye estos argumentos.

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
<td><p><strong>Nombre de formulario</strong></p></td>
<td><p>El nombre del formulario que se va a abrir. El cuadro <strong>Nombre de formulario</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los formularios en la base de datos actual. Este es un argumento obligatorio. Si ejecuta una macro que contiene la acción <strong>AbrirFormulario</strong> en una base de datos de biblioteca, Microsoft Access busca primero el formulario con este nombre en la base de datos de biblioteca y, luego, en la base de datos actual.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Vista</strong></p></td>
<td><p>Vista en la que se abrirá el formulario. Haga clic en <strong>Formulario</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Hoja de datos</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Formulario</strong>.  </p><p><strong>NOTA:</strong>la <STRONG>configuración del</STRONG> argumento View invalida la configuración de las propiedades <STRONG>DefaultView</STRONG> y <STRONG>ViewsAllowed del</STRONG> formulario. For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nombre de filtro</strong></p></td>
<td><p>Filtro que restringe u ordena los registros del formulario. Puede escribir el nombre de una consulta existente o un filtro que se haya guardado como consulta. Sin embargo, la consulta debe incluir todos los campos en el formulario que va a abrir o tener la propiedad <strong>OutputAllFields</strong> establecida en <strong>Sí</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Condición WHERE</strong></p></td>
<td><p>Cláusula WHERE de SQL válida (sin la palabra WHERE) o expresión que Access usa para seleccionar registros de la consulta o tabla subyacente del formulario. Si selecciona un filtro con el argumento <strong>Nombre de filtro</strong>, Access aplica esta cláusula WHERE a los resultados del filtro. Para abrir un formulario y restringir sus registros a los especificados por el valor de un control en otro formulario, use la siguiente expresión: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong> <em>formname</em><strong>]! [</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open. Reemplace <em>nombreDeFormulario</em> y <em>nombre de control en otro formulario</em> con el nombre del otro formulario y el control del otro formulario que contiene el valor con el que desea que coincidan los registros del primer formulario.</p><p><strong>NOTA:</strong>La longitud máxima del argumento <STRONG>Where Condition</STRONG> es de 255 caracteres. If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de datos</strong></p></td>
<td><p>Modo de entrada de datos para el formulario. Esto se aplica solo a los formularios abiertos en la vista Formulario o la vista Hoja de datos. Haga clic en <strong>Agregar</strong> (el usuario puede agregar nuevos registros, pero no puede editar registros existentes), <strong>Editar</strong> (el usuario puede editar registros existentes y agregar nuevos registros), o <strong>Solo lectura</strong> (el usuario solo puede ver registros). El valor predeterminado es <strong>Editar</strong>. <strong>Notas</strong></p>
<ul>
<li><p>La configuración del argumento <strong>Modo de datos</strong> invalida la configuración de las propiedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> y <strong>DataEntry</strong> del formulario. Por ejemplo, si la propiedad <strong>AllowEdits</strong> de un formulario se establece en <strong>No</strong>, aún puede usar la acción <strong>AbrirFormulario</strong> para abrir el formulario en modo Edición.  </p></li>
<li><p>Si deja este argumento en blanco, Access abre el formulario en el modo de entrada de datos establecido por las propiedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> y <strong>DataEntry</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Modo de ventana</strong></p></td>
<td><p>Modo de ventana en el que se abre el formulario. Haga clic en <strong>Normal</strong> (el formulario se abre en el modo establecido por sus propiedades), <strong>Oculto</strong> (el formulario se oculta), <strong>Icono</strong> (el formulario se abre minimizado como una pequeña barra de título en la parte inferior de la pantalla) o <strong>Diálogo</strong> (las propiedades <strong>Modal</strong> y <strong>Emergente</strong> del formulario se establecen en <strong>Sí</strong>). El valor predeterminado es <strong>Normal</strong>.  </p><p><strong>NOTA:</strong>Algunas opciones <STRONG>de configuración de</STRONG> argumentos del Modo de ventana no se aplican al usar documentos con fichas. Para cambiar a ventanas superpuestas:</p>
<ol>
<li><p>Haga clic en la pestaña Archivo y, a continuación, haga clic <strong>en Opciones.</strong></p></li>
<li><p>En el cuadro de diálogo <strong>Opciones de Access</strong>, haga clic en <strong>Base de datos actual</strong>.</p></li>
<li><p>En la sección <strong>Opciones de la</strong>aplicación, en Opciones de ventana de <strong>documento</strong>, haga clic <strong>en Superpuesta de Windows</strong>.</p></li>
<li><p>Haga clic en <strong>Aceptar</strong> y, a continuación, cierre y vuelva a abrir la base de datos.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Esta acción es similar a la de hacer doble clic en un formulario en el panel de navegación o la de hacer clic con el botón derecho en el formulario del panel de navegación y después seleccionar una vista.

Un formulario puede ser modal (se debe cerrar u ocultar para que el usuario pueda realizar cualquier otra acción) o sin modo (el usuario se puede mover a otra ventana mientras se abre el formulario). También puede ser un formulario emergente (un formulario utilizado para recopilar o mostrar información que permanece en la parte superior de todas las demás ventanas de Access). Establezca las propiedades **Modal** y **PopUp** cuando diseñe el formulario. Si usa **Normal** para el argumento **Modo de ventana**, el formulario se abre en el modo especificado por esta configuración de propiedad. Si usa **Diálogo** para el argumento **Modo de ventana**, ambas propiedades se establecen en **Sí**. Un formulario abierto como oculto o como icono se devuelve al modo especificado por su propiedad cuando se muestra o se restaura.

Al abrir un formulario con el argumento **Modo de ventana** establecido en **Diálogo**, Access suspende la macro hasta que el formulario se cierra u oculta. Puede ocultar un formulario estableciendo su propiedad **Visible** en **No** mediante la acción **ConfigurarValor**.

> [!TIP]
> [!SUGERENCIA] Puede seleccionar un formulario en el panel de navegación y arrastrarlo a una fila de acción de macro. Esto crea automáticamente una acción **AbrirFormulario** que abre el formulario en vista Formulario.

El filtro y la condición WHERE que se aplican se convierten en los valores de la propiedad **Filter** del formulario.

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
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Eco activo</strong>: <strong>No</strong></p></td>
<td><p>Detener la actualización de la pantalla mientras se ejecuta la macro.</p></td>
</tr>
<tr class="even">
<td><p><strong>CloseWindow</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>ObjetoFormulario Nombre</strong>: Lista de productos <strong>Guardar</strong>: <strong>No</strong></p></td>
<td><p>Cerrar el formulario Lista de productos</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Formulario Nombre</strong>: Productos <strong>Vista</strong>: <strong>DatosDeFormulario</strong>: <strong>AgregarModo de ventana</strong>: <strong>Normal</strong></p></td>
<td><p>Abrir el formulario Productos.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Elemento</strong>: [Forms]![Products]![SupplierID] <strong>Expresión</strong>: IdProveedor</p></td>
<td><p>Configurar el control Id. de proveedor para el proveedor actual del formulario Proveedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: IdCategoría</p></td>
<td><p>Ir al control Id. de categoría.</p></td>
</tr>
</tbody>
</table>


La siguiente macro abre la lista de productos en la esquina inferior derecha del formulario Proveedores y muestra los productos del proveedor actual. Muestra el uso de las acciones **Eco**, **CuadroDeMensajes**, **IrAControl**, **DetenerMacro**, **AbrirFormulario** y **MoverYCambiarTamañoDeVentana**. También muestra el uso de una expresión condicional con las acciones **CuadroDeMensajes**, **IrAControl** y **DetenerMacro**. Esta macro se debe adjuntar al botón Revisar productos del formulario Proveedores.

**Sincronizar los formularios con una macro**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
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
<td><p><strong>Mensaje</strong>: Mueva al registro de proveedores los productos que quiera ver y haga clic en el botón Revisar productos de nuevo. <strong>Sonido</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Seleccionar un proveedor</p></td>
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
<td><p><strong>Nombre del formulario</strong>: Vista de <strong>lista de productos</strong>: Nombre del filtro de <strong>hoja</strong>de datos : <strong>Condición</strong>Where : [IdDeDe Proveedor] = [Formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></p></td>
<td><p>Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Derecha</strong>: 0,7799 &quot; <strong>Abajo</strong>: 1,8&quot;</p></td>
<td><p>Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</p></td>
</tr>
</tbody>
</table>

