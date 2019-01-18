---
title: EstablecerValor (acción de macro)
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722693"
---
# <a name="setvalue-macro-action"></a>EstablecerValor (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la ación **SetValue** para configurar el valor de un campo, un control o una propiedad de Microsoft Access en un formulario, una hoja de datos del formulario o un informe.

> [!NOTE]
> - [!NOTA] No puede usar la acción **SetValue** para configuar el valor de una propiedad de Access que devuelva un objeto.
> - [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **SetValue** tiene los siguientes argumentos.

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
<td><p><strong>Item</strong></p></td>
<td><p>El nombre del campo, el control o la propiedad cuyo valor quiere configurar. Escriba el nombre del campo, el control o la propiedad en el cuadro <strong>Elemento </strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Debe usar la sintaxis completa para hacer referencia a este elemento, como <em>controlname</em> (para un control en el formulario o el informe desde el que se llamó a la macro) o <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. Se trata de un argumento obligatorio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>La expresión que Access usa para configurar el valor de este elemento. Siempre debe usar la sintaxis completa para hacer referencia a los objetos de la expresión. Por ejemplo, para aumentar el valor de un control Salario de un formulario Empleados en un 10 por ciento, use Forms!Employees!Salary*1.1. Se trata de un argumento obligatorio.</p><p><strong>Nota</strong>: no debe utilizar un signo de igual (=) antes de la expresión en este argumento. Si lo hace, Access evalúa la expresión y, a continuación, utiliza este valor como la expresión en este argumento. Esto puede producir resultados inesperados si la expresión es una cadena.</p>
<p>Por ejemplo, si escribe <strong> = &quot;cadena1&quot; </strong> para este argumento, Access evalúa primero la expresión como Cadena1. A continuación, utiliza Cadena1 como la expresión en este argumento, esperando encontrar un control o una propiedad denominados cadena1 en el formulario o informe que llamó a la macro.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] En una base de datos de Access (.mdb o .accdb), haga clic en el botón **Crear** para usar el Generador de expresiones para crear una expresión para cualquiera de estos argumentos.

## <a name="remarks"></a>Comentarios

Puede usar esta acción para configurar un valor para un campo o un control de un formulario, una hoja de datos de formulario o un informe. También puede configurar el valor de casi todas las propiedades de los controles, formularios e informes de cualquier vista. Para averiguar si una propiedad determinada se puede configurar con una macro y en qué vistas se puede configurar, consulte el tema Ayuda para la propiedad en el Editor de Visual Basic.

También puede configurar el valor de un campo en la tabla subyacente de un formulario, incluso si el formulario no contiene un control enlazado al campo. Use la sintaxis **Forms**\!*formname*\!*fieldname* en el cuadro **elemento** para establecer el valor de ese campo. También puede consultar a un campo de tabla subyacente de un informe mediante el uso de la sintaxis de **informes de**\!*reportname*\!*fieldname*, pero debe haber un control del informe enlazado a este campo o el campo debe hacer referencia a un control calculado en el informe.

Si configura el valor de un control en un formulario, la acción **SetValue** no desencadena las reglas de validación de nivel de formulario del control, pero desencadena las reglas de validación de nivel de tabla del campo subyacente si el control es un control enlazado. La acción **SetValue** también desencadena la actualización, pero puede que no se produzca de forma inmediata. Para desencadenar la actualización inmediatamente y forzar la finalización de la actualización, use la acción **RepaintObject**. El valor que se configura en un control con la acción **SetValue** tampoco se ve afectada por una máscara de entrada configurada en la propiedad **InputMask** del control o del campo subyacente.

Para cambiar el valor de un control, puede usar la acción **SetValue** en una macro especificada por la propiedad de evento **AfterUpdate** del control. Sin embargo, no puede usar la acción **SetValue** en una macro especificada por una propiedad de evento **BeforeUpdate** del control para cambiar el valor del control (aunque puede usar la acción **SetValue** para cambiar el valor de otros controles). También puede usar la acción **SetValue** en una macro especificada por la propiedad **BeforeUpdate** o **AfterUpdate** de un formulario para cambiar el valor de los controles del registro actual.

> [!NOTE]
> No puede usar la acción **SetValue** para configurar el valor de los siguientes controles:
> - Controles enlazados y calculados en informes.
> - Controles calculados en formularios.

> [!TIP]
> [!SUGERENCIA] Puede usar la acción **SetValue** para ocultar o mostrar un formulario en la vista Formulario. ¡Escriba **formularios**! formname ****. Visible** en el cuadro **elemento** y **No** o **Sí** en el cuadro **expresión** . Configurar una propiedad **Visible** de un formulario modal en **No** oculta el formulario y lo convierte en no modal. Configurar la propiedad en **Sí** muestra el formulario y lo convierte en modal de nuevo.

Cambiar el valor de o agregar nuevos datos a un control mediante la acción **SetValue** en una macro no desencadena eventos como **BeforeUpdate**, **BeforeInsert** o **Change** que ocurren al cambiar o introducir datos en estos controles en la interfaz de usuario. Estos eventos tampoco ocurren si configura el valor del control con un módulo de Visual Basic para aplicaciones (VBA).

Esta acción no está disponible en un módulo de VBA. Configure el valor directamente en VBA.

## <a name="example"></a>Ejemplo

**Configurar el valor de un control con una macro**

La siguiente macro abre el formulario Agregar productos desde un botón del formulario Proveedores. Muestra el uso de las acciones **Eco**, **CerrarVentana**, **AbrirFormulario**, **ConfigurarValor** e **IrAControl**. La acción **SetValue** configura el control Id. de proveedor en el formulario Productos para el proveedor actual del formulario Proveedores. La acción **IrAControl** mueve el foco al campo Id. de categoría, donde puede empezar a introducir los datos para el nuevo producto. Esta macro se debe adjuntar al botón Agregar productos del formulario Proveedores.

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
<td><p>Configurar el control IdProveedor el proveedor actual del formulario Proveedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nombre del control</strong>: IdCategoría</p></td>
<td><p>Ir al control Id.</p></td>
</tr>
</tbody>
</table>

