---
title: 'HelloData: Una aplicación de ADO simple'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292023"
---
# <a name="hellodata-a-simple-ado-application"></a>HelloData: Una aplicación de ADO simple

**Se aplica a:** Access 2013, Office 2013

Para establecer el trabajo de base de una exploración de la biblioteca ADO, considere la opción de utilizar una aplicación ADO simple denominada "HelloData". HelloData ejecuta cada una de las cuatro operaciones principales de ADO (obtener, examinar, editar y actualizar datos). Para centrarse en los conceptos básicos de ADO y evitar la sobrecarga de código, se realiza un mínimo tratamiento de errores en este ejemplo.

La aplicación realiza consultas en la base de datos de ejemplo Neptuno que se incluye con Microsoft SQL Server 2000.

**Para ejecutar HelloData**

1.  Cree un nuevo proyecto estándar ejecutable de Visual Basic que haga referencia a la biblioteca de ADO 2.5.

2.  Cree cuatro botones de comando en la parte superior del formulario, estableciendo las propiedades **Name** y **Caption** en los valores que se muestran en la tabla que figura más abajo.

3.  Debajo de los botones, agregue un **control cuadrícula de datos de Microsoft** (Msdatgrd.ocx). El archivo Msdatgrd.ocx viene con Visual Basic y se encuentra en el directorio \\ de windows \\ system32 \\ o winnt \\ system32. Para agregar el control cuadrícula de datos al panel de cuadro de herramientas de Visual Basic, seleccione **Componentes** en el menú **Proyecto**. A continuación, compruebe el cuadro situado junto a "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" y haga clic en **Aceptar**. Para agregar el control al proyecto, arrastre el control cuadrícula de datos desde el cuadro de herramientas hasta el formulario de Visual Basic.

4.  Cree un control **cuadro de texto** en el formulario debajo de la cuadrícula y establezca sus propiedades tal como se muestra en la tabla. El formulario debe tener un aspecto similar a la ilustración siguiente cuando haya finalizado.

5.  Por último, copie el código enumerado en [HelloData Code](hellodata-code.md) y péguelo en la ventana del editor de código del formulario. Presione **F5** para que se ejecute el código.

> [!NOTE]
> [!NOTA] En el ejemplo siguiente y en toda la Guía, se utiliza el identificador de usuario "MyId" con la contraseña "123aBc" para autenticación en el servidor. Debe sustituir estos valores con credenciales de inicio de sesión válidas para su servidor. Sustituya también el valor "MyServer" por el nombre del servidor.

Para obtener una descripción detallada del código, vea [HelloData Details](hellodata-details.md).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de control</p></th>
<th><p>Propiedad</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Form</p></td>
<td><p>Nombre</p></td>
<td><p>Form1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Height</p></td>
<td><p>6500</p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p>Width</p></td>
<td><p>6500</p></td>
</tr>
<tr class="even">
<td><p>Cuadrícula de datos de MS</p></td>
<td><p>Nombre</p></td>
<td><p>grdDisplay1</p></td>
</tr>
<tr class="odd">
<td><p>TextBox</p></td>
<td><p>Nombre</p></td>
<td><p>txtDisplay1</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Multilínea</p></td>
<td><p>true</p></td>
</tr>
<tr class="odd">
<td><p>Botón de comando</p></td>
<td><p>Nombre</p></td>
<td><p>cmdGetData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Get Data</p></td>
</tr>
<tr class="odd">
<td><p>Botón de comando</p></td>
<td><p>Nombre</p></td>
<td><p>cmdExamineData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Examine Data</p></td>
</tr>
<tr class="odd">
<td><p>Botón de comando</p></td>
<td><p>Nombre</p></td>
<td><p>cmdEditData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Edit Data</p></td>
</tr>
<tr class="odd">
<td><p>Botón de comando</p></td>
<td><p>Nombre</p></td>
<td><p>cmdUpdateData</p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p>Caption</p></td>
<td><p>Update Data</p></td>
</tr>
</tbody>
</table>



