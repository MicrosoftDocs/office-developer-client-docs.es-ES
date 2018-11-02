---
title: MoverYCambiarTamañoDeVentana (acción de macro)
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd5bbe18af823e2b36772ef209db18ba6cb4b1d4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925271"
---
# <a name="moveandsizewindow-macro-action"></a>MoverYCambiarTamañoDeVentana (acción de macro)


**Se aplica a**: Access 2013, Office 2013


Si ha establecido el documento de opciones de la ventana para usar ventanas superpuestas en lugar de documentos con fichas, puede utilizar la acción **Moverycambiartamañodeventana** para mover o cambiar el tamaño de la ventana activa. Para obtener información acerca de cómo configurar las opciones de la ventana de documento, vea la sección Comentarios.

## <a name="setting"></a>Configuración

La acción **Moverycambiartamañodeventana** tiene los siguientes argumentos.

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
<td><p><strong>Right</strong></p></td>
<td><p>Nueva posición horizontal de la esquina superior izquierda de la ventana, medida desde el borde izquierdo de la ventana contenedora. Especifique la posición en el cuadro de la <strong>derecha</strong> en la sección <strong>Argumentos de acción</strong> del panel Generador de macros.</p></td>
</tr>
<tr class="even">
<td><p><strong>Down</strong></p></td>
<td><p>Nueva posición vertical de la esquina superior izquierda de la ventana, medida desde el borde superior de la ventana contenedora.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Width</strong></p></td>
<td><p>Nuevo ancho de la ventana.</p></td>
</tr>
<tr class="even">
<td><p><strong>Height</strong></p></td>
<td><p>Nuevo alto de la ventana.</p></td>
</tr>
</tbody>
</table>


Si deja un argumento en blanco, Microsoft Access utiliza la configuración actual de la ventana.

Debe escribir un valor para al menos un argumento.


> [!NOTE]
> <P>Cada medida es en pulgadas o centímetros, dependiendo de la configuración regional en el Panel de Control de Windows.</P>



## <a name="remarks"></a>Comentarios

Para configurar una aplicación para utilizar ventanas superpuestas en lugar de documentos con fichas, utilice el procedimiento siguiente:

1.  y, a continuación, haga clic en **Opciones**

2.  Haga clic en **base de datos actual**.

3.  En la sección **Opciones de aplicación**, bajo **Opciones de la ventana de documentos**, haga clic en **Ventanas superpuestas**.

4.  Haga clic en **Aceptar**y, a continuación, cierre y vuelva a abrir la base de datos.

Esta acción es similar a hacer clic en **mover** o **tamaño** en el menú **Control** de la ventana. Con los comandos de menú, se utilizan las teclas de desplazamiento para mover o cambiar el tamaño de la ventana. Con la acción **Moverycambiartamañodeventana** , introduzca directamente las medidas de posición y tamaño. También puede usar el mouse para mover y cambiar el tamaño de windows.

Puede usar esta acción en cualquier ventana, en cualquier vista.

**Sugerencias**

  - Para mover una ventana sin cambiar su tamaño, especifique valores para la **derecha** y **abajo** argumentos pero deja en blanco los argumentos **ancho** y **alto** .

  - Para cambiar el tamaño de una ventana sin moverla, especifique valores para los argumentos de **alto** y **ancho** pero deja en blanco los argumentos **derecha** y **abajo** .

Para ejecutar la acción **Moverycambiartamañodeventana** en un módulo Visual Basic para aplicaciones (VBA), use el método **MoveSize** del objeto **DoCmd** .

## <a name="example"></a>Ejemplo

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
<td><p></p></td>
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

