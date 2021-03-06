---
title: IrARegistro (acción de macro)
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292142"
---
# <a name="gotorecord-macro-action"></a>IrARegistro (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **IrARegistro** para convertir el registro especificado en el registro activo de una tabla abierta, un formulario abierto o el conjunto de resultados de una consulta abierta.

## <a name="setting"></a>Configuración

La acción **IrARegistro** tiene los siguientes argumentos.

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
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>Tipo de objeto que contiene el registro que se desea convertir en registro activo. Haga clic en <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Vista de servidor</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Deje este argumento en blanco para seleccionar el objeto activo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>Nombre del objeto que contiene el registro que se desea convertir en registro activo. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos de la base de datos activa que sean del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si deja en blanco el argumento <strong>Tipo de objeto</strong>, deje también en blanco este argumento.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>Registro que se va a convertir en registro activo. Haga clic en <strong>Anterior</strong>, <strong>Siguiente</strong>, <strong>Primero</strong>, <strong>Último</strong>, <strong>Ir a</strong> o <strong>Nuevo</strong> en el cuadro <strong>Registro</strong>. El valor predeterminado es <strong>Siguiente</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>Número entero o expresión que se evalúa como un número entero. Una expresión debe ir precedida de un signo igual ( <strong>=</strong> ). Este argumento especifica el registro que pasa a ser el registro activo. El argumento <strong>Desplazamiento</strong> puede usarse de dos formas:</p>
<ul>
<li><p>Cuando el valor del argumento <strong>Registro</strong> es <strong>Siguiente</strong> o <strong>Anterior</strong>, Microsoft Office Access 2007 se mueve hacia delante o hacia atrás el número de registros especificado en el argumento <strong>Desplazamiento</strong>.</p></li>
<li><p>Cuando el valor del argumento <strong>Registro</strong> es <strong>Ir a</strong>, Access se desplaza al registro que tenga el mismo número que el argumento <strong>Desplazamiento</strong>. El número de registro se muestra en el cuadro de número de registro situado en la parte inferior de la ventana.</p>
<p><strong>NOTA</strong>: Si usa la configuración <strong>First</strong>, <strong>Last</strong>o <strong>New</strong> para el argumento <strong>Record,</strong> Access omite el <strong>argumento Offset.</strong> Si se especifica para el argumento <strong>Desplazamiento</strong> un valor excesivo, Access muestra un mensaje de error. No se pueden especificar números negativos para el argumento <strong>Desplazamiento</strong>.</p></li>
<li><p>Cuando el valor del argumento <strong>Registro</strong> es <strong>Siguiente</strong> o <strong>Anterior</strong>, Microsoft Office Access 2007 se mueve hacia delante o hacia atrás el número de registros especificado en el argumento <strong>Desplazamiento</strong>.</p></li>
<li><p>Cuando el valor del argumento <strong>Registro</strong> es <strong>Ir a</strong>, Access se desplaza al registro que tenga el mismo número que el argumento <strong>Desplazamiento</strong>. El número de registro se muestra en el cuadro de número de registro situado en la parte inferior de la ventana.</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Si el enfoque está en un control determinado de un registro, esta acción lo deja en el mismo control del nuevo registro.

Se puede usar el valor **Nuevo** para el argumento **Registro** para ir al registro en blanco situado al final de un formulario o una tabla de manera que se puedan escribir nuevos datos.

Esta acción es similar a hacer clic en la flecha situada debajo del botón **Buscar** en la ficha **Inicio** y, a continuación, hacer clic en **Ir a**. Los subcomandos **Primero**, **Último**, **Siguiente**, **Anterior** y **Nuevo registro** del comando **Ir a** tienen el mismo efecto en el objeto seleccionado que los valores **Primero**, **Último**, **Siguiente**, **Anterior** y **Nuevo** del argumento **Registro**. Asimismo, puede moverse a registros mediante los botones de navegación situados en la parte inferior de la ventana.

Puede usar la acción **IrARegistro** para convertir un registro de un formulario oculto en registro activo si especifica el formulario oculto en los argumentos **Tipo de objeto** y **Nombre del objeto**.

Para ejecutar la acción **IrARegistro** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **GoToRecord** del objeto **DoCmd**.

