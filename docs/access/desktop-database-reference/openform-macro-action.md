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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707629"
---
# <a name="openform-macro-action"></a>AbrirFormulario (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **AbrirFormulario** para abrir un formulario en la vista Formulario, Diseño, Vista preliminar u Hoja de datos. Puede seleccionar los modos de entrada de datos y ventana para el formulario y restringir los registros que se muestra en él.

## <a name="setting"></a>Configuración

La acción **AbrirFormulario** incluye estos argumentos.

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
<td><p><strong>Nombre de formulario</strong></p></td>
<td><p>El nombre del formulario que se va a abrir. El cuadro <strong>Nombre de formulario</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros muestra todos los formularios en la base de datos actual. Este es un argumento obligatorio. Si ejecuta una macro que contiene la acción <strong>AbrirFormulario</strong> en una base de datos de biblioteca, Microsoft Access busca primero el formulario con este nombre en la base de datos de biblioteca y, luego, en la base de datos actual.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Vista</strong></p></td>
<td><p>Vista en la que se abrirá el formulario. Haga clic en <strong>Formulario</strong>, <strong>Diseño</strong>, <strong>Vista preliminar</strong>, <strong>Hoja de datos</strong>, <strong>Tabla dinámica</strong> o <strong>Gráfico dinámico</strong> en el cuadro <strong>Vista</strong>. El valor predeterminado es <strong>Formulario</strong>.  </p><p><strong>Nota</strong>: el valor del argumento <STRONG>vista</STRONG> reemplaza los valores de las propiedades del formulario <STRONG>DefaultView</STRONG> y <STRONG>ViewsAllowed</STRONG> . Por ejemplo, si la propiedad <STRONG>ViewsAllowed</STRONG> de un formulario se establece en la <STRONG>hoja de datos</STRONG>, puede usar la acción <STRONG>AbrirFormulario</STRONG> para abrir el formulario en la vista formulario.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nombre de filtro</strong></p></td>
<td><p>Filtro que restringe u ordena los registros del formulario. Puede escribir el nombre de una consulta existente o un filtro que se haya guardado como consulta. Sin embargo, la consulta debe incluir todos los campos en el formulario que va a abrir o tener la propiedad <strong>OutputAllFields</strong> establecida en <strong>Sí</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Condición WHERE</strong></p></td>
<td><p>Cláusula WHERE de SQL válida (sin la palabra WHERE) o expresión que Access usa para seleccionar registros de la consulta o tabla subyacente del formulario. Si selecciona un filtro con el argumento <strong>Nombre de filtro</strong>, Access aplica esta cláusula WHERE a los resultados del filtro. Para abrir un formulario y restringir sus registros a los especificados por el valor de un control de otro formulario, utilice la siguiente expresión: <strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong> <em>FormName</em> <strong>]! [</strong><em>controlname en otro formulario</em><strong>]</strong> sustituya <em>fieldname</em> por el nombre de un campo en la tabla o consulta subyacente del formulario que desea abrir. Reemplace <em>nombreDeFormulario</em> y <em>nombrecontrol en otro formulario</em> con el nombre de otro formulario y el control del otro formulario que contiene el valor que desea en el primer formulario para que coincida con los registros.</p><p><strong>Nota</strong>: la longitud máxima del argumento <STRONG>Condición Where</STRONG> es de 255 caracteres. Si necesita escribir una cláusula WHERE de SQL más compleja y más larga, utilice el método <STRONG>OpenForm</STRONG> del objeto <STRONG>DoCmd</STRONG> en un de Visual Basic para aplicaciones (VBA) en su lugar. Puede especificar instrucciones de cláusula WHERE de SQL de hasta 32.768 caracteres en VBA.</p></td>
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
<td><p>Modo de ventana en el que se abre el formulario. Haga clic en <strong>Normal</strong> (el formulario se abre en el modo establecido por sus propiedades), <strong>Oculto</strong> (el formulario se oculta), <strong>Icono</strong> (el formulario se abre minimizado como una pequeña barra de título en la parte inferior de la pantalla) o <strong>Diálogo</strong> (las propiedades <strong>Modal</strong> y <strong>Emergente</strong> del formulario se establecen en <strong>Sí</strong>). El valor predeterminado es <strong>Normal</strong>.  </p><p><strong>Nota</strong>: algunos valores del argumento <STRONG>Modo de la ventana</STRONG> no se aplican al uso de documentos con fichas. Para cambiar a ventanas superpuestas:</p>
<ol>
<li><p>Haga clic en la pestaña archivo y, a continuación, haga clic en <strong>Opciones</strong>.</p></li>
<li><p>En el cuadro de diálogo <strong>Opciones de Access</strong>, haga clic en <strong>Base de datos actual</strong>.</p></li>
<li><p>En la sección <strong>Opciones de la aplicación</strong>, en <strong>Opciones de la ventana de documentos</strong>, haga clic en <strong>Ventanas superpuestas</strong>.</p></li>
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
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></p></td>
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
<td><p>IsNull([IdProveedor])</p></td>
<td><p><strong>CuadroDeMensajes</strong></p></td>
<td><p><strong>Mensaje</strong>: mover al registro del proveedor los productos que quiera ver, luego, haga clic de nuevo en el botón Revisar productos. <strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: seleccionar un proveedor</p></td>
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
<td><p><strong>DetenerMacro</strong></p></td>
<td><p></p></td>
<td><p>Detener la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de producto: <strong>Nombre DatasheetFilter</strong>: <strong>condición Where</strong>: [Id] = [formularios]! [Proveedores]! [SupplierID] <strong>Modo de datos</strong>: <strong>Modo de lectura OnlyWindow</strong>: <strong>Normal</strong></p></td>
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

