---
title: MoverYCambiarTamañoDeVentana (acción de macro)
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288809"
---
# <a name="moveandsizewindow-macro-action"></a>MoverYCambiarTamañoDeVentana (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Si ha establecido las opciones de la ventana de documento para usar ventanas superpuestas en lugar de documentos con fichas, puede usar la acción **moverycambiartamañodeventana** para mover o cambiar el tamaño de la ventana activa. Para obtener información sobre cómo establecer las opciones de la ventana de documento, vea la sección Comentarios.

## <a name="setting"></a>Configuración

La acción **moverycambiartamañodeventana** tiene los siguientes argumentos.

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
<td><p>Nueva posición horizontal de la esquina superior izquierda de la ventana, medida desde el borde izquierdo de la ventana contenedora. Escriba la posición en el cuadro <strong>derecha</strong> en la sección <strong>argumentos de acción</strong> del panel generador de macros.</p></td>
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
> Cada medida se encuentra en pulgadas o centímetros, en función de la configuración regional del panel de control de Windows.

## <a name="remarks"></a>Comentarios

Para configurar una aplicación para que use ventanas superpuestas en lugar de documentos con fichas, use el procedimiento siguiente:

1.  Haga clic en **Opciones**

2.  Haga clic en **base de datos actual**.

3.  En la sección **Opciones de aplicación**, bajo **Opciones de la ventana de documentos**, haga clic en **Ventanas superpuestas**.

4.  Haga clic en **Aceptar**y, a continuación, cierre y vuelva a abrir la base de datos.

Esta acción es similar a hacer clic en **mover** o **tamaño** en el menú **control** de la ventana. Con los comandos de menú, puede usar las teclas de flecha del teclado para mover o cambiar el tamaño de la ventana. Con la acción **moverycambiartamañodeventana** , se especifican las medidas de posición y tamaño directamente. También puede usar el mouse para mover y cambiar el tamaño de las ventanas.

Puede usar esta acción en cualquier ventana, en cualquier vista.

> [!TIP]
> - Para mover una ventana sin cambiar su tamaño, escriba valores para los argumentos **derecha** y **abajo** , pero deje los argumentos **ancho** y **alto** en blanco.
> - Para cambiar el tamaño de una ventana sin moverla, escriba valores para los argumentos **width** y **height** , pero deje los argumentos **right** y **Down** en blanco.

Para ejecutar la acción **moverycambiartamañodeventana** en un módulo de Visual Basic para aplicaciones (VBA), use el método **MoveSize** del objeto **DoCmd** .

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
<th><p>Comment</p></th>
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
<td><p><strong>Mensaje</strong>: Mueva al registro de proveedores los productos que quiera ver y haga clic en el botón Revisar productos de nuevo. <strong>Bip</strong>: <strong>SíTipo</strong>: <strong>ningunotítulo</strong>: seleccionar un proveedor</p></td>
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
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>Detener la macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nombre del formulario</strong>: <strong>vista</strong>de lista de productos: <strong>datosnombre Name</strong>: <strong>Where condición</strong>: [ID de proveedor] = [formularios]! [Proveedores] IdProveedor <strong>Modo de datos</strong>: <strong>lectura modo lecturamodo</strong>: <strong>normal</strong></p></td>
<td><p>Abrir el formulario Lista de productos y mostrar los productos del proveedor actual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moverycambiartamañodeventana</strong></p></td>
<td><p><strong>derecha</strong>: 0,7799&quot; <strong>abajo</strong>: 1,8&quot;</p></td>
<td><p>Coloque el formulario Lista de productos en la esquina inferior derecha del formulario Proveedores.</p></td>
</tr>
</tbody>
</table>

