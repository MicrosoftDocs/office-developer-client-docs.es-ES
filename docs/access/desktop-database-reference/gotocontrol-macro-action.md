---
title: IrAControl (acción de macro)
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292170"
---
# <a name="gotocontrol-macro-action"></a>IrAControl (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **IrAControl** para desplazar el enfoque al campo o control especificado en el registro actual del formulario abierto, la hoja de de formulario, la hoja de usuario de tabla o la hoja de consulta de la consulta. Puede usar esta acción si desea que un campo o control concreto tenga el foco. Después, puede usar el campo o control para comparaciones o acciones **FindRecord**. También puede usar esta acción para desplazarse por un formulario según ciertas condiciones. Por ejemplo, si el usuario escribe No en un control Casado en un formulario de seguros de salud, el foco puede omitir automáticamente el control Nombre de cónyuge y pasar al siguiente control.

## <a name="setting"></a>Configuración

> [!NOTE]
> Esta acción no está disponible para su uso con páginas de acceso a datos.

La acción **GoToControl** tiene el siguiente argumento.

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
<td><p><strong>Nombre del control</strong></p></td>
<td><p>El nombre del campo o control donde desea el foco. Escriba el nombre del campo o control en el cuadro <strong>nombre del control</strong> en la sección <strong>argumentos de acción</strong> del panel generador de macros. Este es un argumento obligatorio.</p>
<p><strong>Nota</strong>: escriba solo el nombre del campo o control en el argumento <strong>nombre del control</strong> , no el identificador completo, como Forms! Productos! [Identificador de producto].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

No puede usar la acción **GoToControl** para mover el enfoque a un control de un formulario oculto.

> [!TIP]
> Puede usar la acción **GoToControl (IrAControl** ) para moverse a un subformulario, que es un tipo de control. A continuación, puede usar la acción **IrARegistro** para desplazarse a un registro determinado en el subformulario. También puede moverse a un control de un subformulario mediante la acción **GoToControl (IrAControl** ) para desplazarse primero al subformulario y, después, al control del subformulario.

Para ejecutar la acción **IrAControl** en un módulo de Visual Basic para aplicaciones (VBA), use el método **GoToControl** del objeto **DoCmd** . También puede usar el método **SetFocus** para desplazar el enfoque a un control de un formulario o a cualquiera de sus subformularios, o a un campo de una tabla abierta, una consulta o una hoja de de de formulario abierta.

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
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Eco</strong></p></td>
<td><p><strong>Eco activo</strong>: <strong>No</strong></p></td>
<td><p>Detener la actualización de la pantalla mientras se ejecuta la macro.</p></td>
</tr>
<tr class="even">
<td><p><strong>Cerrarventana</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>nombre de formularionombre</strong>: lista de productos <strong>Guardar</strong>: <strong>no</strong></p></td>
<td><p>Cierre el formulario lista de productos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: productos <strong>vista</strong>: <strong>formulariomodo Mode</strong>: <strong>agregarmodo Mode</strong>: <strong>normal</strong></p></td>
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


**Validar los datos con una macro**

La siguiente macro de validación comprueba los códigos postales introducidos en el formulario Proveedores. Muestra el uso de las acciones **DetenerMacro**, **CuadroDeMensajes**, **CancelarEvento** e **IrAControl**. Una expresión condicional comprueba el país o la región y el código postal especificados en un registro del formulario. Si el código postal no tiene el formato correcto para el país o la región, la macro muestra un cuadro de mensaje y cancela el proceso de guardar el registro. A continuación, la macro vuelve al control código postal, donde puede corregir el error. Esta macro se debe adjuntar a la propiedad **BeforeUpdate** del formulario Proveedores.

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
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull ([PaísRegión])</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Si PaísRegión es <strong>null</strong>, no se podrá validar el código postal.</p></td>
</tr>
<tr class="even">
<td><p>CountryRegion In (&quot;Francia&quot;,&quot;Italia&quot;,&quot;España&quot;) y Len ([código postal]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: el código postal debe ser de 5 caracteres. <strong>Bip</strong>: <strong>SíTipo</strong>: <strong>informacióntítulo</strong>: error de código postal</p></td>
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
<td><p>CountryRegion En (&quot;Australia&quot;,&quot;Singapur&quot;) y longitud ([código postal]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p>Mensaje: el código postal debe tener 4 caracteres. <strong>Bip</strong>: <strong>SíTipo</strong>: <strong>informacióntítulo</strong>: error de código postal</p></td>
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
<td><p>([PaísRegión] = &quot;Canadá&quot;) And ([código postal] no like&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Mensaje</strong>: El código postal no es válido. Ejemplo de código canadiense: H1J 1C3 <strong>beep</strong>: <strong>SíTipo</strong>: <strong>informacióntítulo</strong>: error de código postal</p></td>
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

