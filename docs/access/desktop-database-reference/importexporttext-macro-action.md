---
title: ImportarExportarTexto (acción de macro)
TOCTitle: ImportExportText macro action
ms:assetid: 366fa095-6f09-7c22-e734-bfa585cfe79e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192475(v=office.15)
ms:contentKeyID: 48544171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168097
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a26b370e14dba68b0cbe686f4b23ae0db3fc1fea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707867"
---
# <a name="importexporttext-macro-action"></a>ImportarExportarTexto (acción de macro)

**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **ImportarExportarTexto** para importar o exportar texto entre la base de datos activa de Microsoft Access (.mdb o .accdb) o un proyecto de Access (.adp) y un archivo de texto. También puede vincular los datos en un archivo de texto a una base de datos de Access activa. Con un archivo de texto vinculado, puede ver los datos del texto con Access y tener al mismo tiempo completo acceso a los datos desde su programa de procesamiento de textos. También puede importar desde, exportar a y vincular a una tabla o lista en un archivo HTML (\*.html).

> [!NOTE]
> [!NOTA] Si establece un vínculo con los datos de un archivo de texto o de un archivo HTML, los datos en Access son de solo lectura. [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **ImportarExportarTexto** utiliza los siguientes argumentos.

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
<td><p><strong>Tipo de transferencia</strong></p></td>
<td><p>El tipo de transferencia que quiera realizar. Puede importar, exportar o vincular datos en archivos de texto delimitados, de ancho fijo o HTML. También puede exportar datos a un archivo de datos de combinación de correspondencia de Microsoft Word, que puede usar con la característica de combinación de correspondencia para crear documentos combinados, como cartas modelo o etiquetas postales. Seleccione <strong>Importar delimitado</strong>, <strong>Importar ancho fijo</strong>, <strong>Importar HTML</strong>, <strong>Exportar delimitado</strong>, <strong>Exportar ancho fijo</strong>, <strong>Exportar HTML</strong>, <strong>Exportar Word para combinación de Windows</strong>, <strong>Vincular delimitado</strong>, <strong>Vincular ancho fijo</strong> o <strong>Vincular HTML</strong> en el cuadro <strong>Tipo de transferencia</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. El valor predeterminado es <strong>Importar delimitado</strong>.  </p><p><strong>Nota</strong>: tipos de transferencia <STRONG>Importar delimitado</STRONG>, <STRONG>Importar ancho fijo</STRONG>, <STRONG>Exportar delimitado</STRONG>, <STRONG>Exportar ancho fijo</STRONG>o <STRONG>Exportar combinación de Word para Windows</STRONG> sólo se admiten en un proyecto de Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre de especificación</strong></p></td>
<td><p>El nombre de especificación para el conjunto de opciones que determinan cómo se importa, exporta o vincula un archivo de texto. Para un archivo de texto de ancho fijo, deberá especificar un argumento o utilizar un archivo schema.ini, el cual deberá almacenarse en la misma carpeta que el archivo de texto importado o vinculado.  </p>
<p>Para crear una especificación para importar o vincular un archivo de texto:</p>
<ol>
<li><p>En el cuadro de diálogo <strong>Obtener datos externos</strong>, especifique la ruta de acceso del archivo de texto de origen en el cuadro <strong>Nombre de archivo</strong>.</p></li>
<li><p>Seleccione la opción que desee para almacenar los datos (importar, anexar o vincular) y haga clic en <strong>Aceptar</strong>.</p></li>
<li><p>En el cuadro de diálogo <strong>Asistente para importación de texto</strong>, haga clic en <strong>Avanzadas</strong>.</p></li>
<li><p>Especifique las opciones que desee para esta especificación y, a continuación, haga clic en <strong>Guardar como</strong>.</p></li>
<li><p>Escriba el nombre que desee para la especificación y haga clic en <strong>Aceptar</strong>.</p></li>
<li><p>Puede administrar especificaciones existentes haciendo clic en <strong>Especificaciones</strong> en el cuadro de diálogo.</p></li>
<li><p>Haga clic en <strong>Aceptar</strong> para cerrar el cuadro de diálogo de especificaciones.</p></li>
</ol>
<p></p>
<p>A continuación, puede escribir el nombre de la especificación en este argumento cuando quiera importar o exportar el mismo tipo de archivo de texto. Puede importar, exportar o vincular archivos de texto delimitado sin escribir un nombre de especificación para este argumento. En este caso, Access usa los valores predeterminados del cuadro de diálogo del asistente. Access usa un formato predeterminado para los archivos de datos de combinación de correspondencia y, por tanto, no es necesario escribir un nombre de especificación para este argumento al exportar estos tipos de archivos. Puede usar las especificaciones de importación y exportación con los archivos HTML, pero la única parte de la especificación que se aplica es la especificación para el formato del tipo de datos.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nombre de la tabla</strong></p></td>
<td><p>El nombre de la tabla de Access a la que importar los datos de texto, desde la que exportar el formulario de datos o a la que vincular los datos de texto. También puede escribir el nombre de la consulta de Access desde la que quiere exportar los datos. Se trata de un argumento obligatorio. Si hace clic en <strong>Importar delimitado</strong>, <strong>Importar ancho fijo</strong> o <strong>Importar HTML</strong> del cuadro <strong>Tipo de transferencia</strong>, Access anexa los datos de texto a esta tabla, si existe. De lo contrario, Access crea una nueva tabla con los datos de texto. No puede usar una instrucción SQL para especificar los datos para exportar al usar la acción <strong>ImportarExportarTexto</strong>. En lugar de usar una instrucción SQL, primero debe crear una consulta y especificar el nombre la consulta en el argumento <strong>Nombre de tabla</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del archivo</strong></p></td>
<td><p>El nombre del archivo de texto desde el que importar, exportar a o vincular. Incluir la ruta de acceso completa. Se trata de un argumento obligatorio. Access crea un nuevo archivo de texto al exportar los datos desde Access. Si el nombre del archivo es el mismo que el de un archivo existente, Access reemplaza el archivo de texto existente. Si quiere importar o vincular una tabla o una lista concreta a un archivo HTML, puede usar el argumento <strong>Nombre de tabla HTML</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Contiene nombres de campo</strong></p></td>
<td><p>Especifica si la primera fila del archivo de texto contiene los nombres de los campos. Si selecciona <strong>Sí</strong>, Access utiliza los nombres de esta fila como nombres de campos de la tabla de Access al importar o vincular los datos de texto. Si selecciona <strong>No</strong>, Access trata la primera fila como una fila normal de datos. El valor predeterminado es <strong>No</strong>. 

<br/><br/>Access ignora este argumento para los archivos de datos de combinación de correspondencia de Word para Windows porque la primera fila debe contener los nombres de campo. Al exportar una tabla de Access o seleccionar una consulta para un archivo de texto delimitado o de ancho fijo, Access inserta los nombre de campo de la tabla o de la consulta de selección en la primera fila el archivo de texto, si selecciona <strong>Sí</strong> para este argumento.<br/><br/>Si está importando o vinculando un archivo de texto de ancho fijo y selecciona <strong>Sí</strong> en este cuadro, la primera fila, que contiene los nombres de los campos, debe usar el delimitador de campos establecido en la especificación de importación y exportación para separar los nombres de los campos. Si va a exportar los datos a un archivo de texto de ancho fijo y selecciona <strong>Sí</strong> para este argumento, Access inserta los nombres de los campos en la primera fila del archivo de texto con este delimitador.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre de tabla HTML</strong></p></td>
<td><p>El nombre de la tabla o lista del archivo HTML que desea importar o vincular. Este argumento no se tiene en cuenta a menos que el argumento <strong>Tipo de transferencia</strong> presente el valor Importar HTML o Vincular HTML. Si deja en blanco este argumento, se importará o vinculará la primera tabla o lista del archivo HTML. 

<br/><br/>El nombre de tabla o lista en el archivo HTML se determina por el texto especificado por el &lt;título&gt; etiqueta, si no hay un &lt;título&gt; etiqueta. Si no hay ninguna etiqueta &lt;TÍTULO&gt;, el nombre de etiqueta está determinado por el texto especificado por la etiqueta &lt;TÍTULO&gt;. Si más de una tabla o lista con el mismo nombre, Access las distingue agregando un número al final de cada nombre; Por ejemplo, Empleados1 y Empleados2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Página de códigos</strong></p></td>
<td><p>El nombre del juego de caracteres que se usa con la página de códigos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede exportar los datos de consultas de selección de Access a archivos de texto. Access exporta el conjunto de resultados de la consulta, tratándolo como si fuera una tabla.

Los datos de texto que se anexan a una tabla de Access existente deben ser compatibles con la estructura de la tabla.

- Cada campo del texto debe ser del mismo tipo de datos que el campo correspondiente de la tabla.

- Los campos deben estar en el mismo orden (a menos que haya establecido el argumento **Contiene nombres de campo** en **Sí**, en cuyo caso los nombres de los campos del texto deben coincidir con los nombres de los campos de la tabla).

Esta acción es similar a hacer clic en **Archivo de texto** en el grupo **Importar** o **Exportar** en la ficha **Datos externos**. Los argumentos de la acción **ImportarExportarTexto** reflejan las opciones del asistente abierto por el comando **Archivo de texto**.

> [!TIP]
> [!SUGERENCIA] Una especificación de importación o exportación almacena la información que Access necesita para importar, exportar o vincular un archivo de texto. Puede usar la especificación almacenada para importar, exportar o vincular datos de texto desde o hacia archivos de texto similares. Por ejemplo, podría recibir cifras semanales de ventas en un archivo de texto desde un gran sistema (mainframe). Entonces, puede crear y guardar una especificación para este tipo de datos y usarla siempre que agregue estos datos a la base de datos de Access.

> [!NOTE]
> [!NOTA] Si consulta o filtra un archivo de texto vinculado, la consulta o el filtro distinguen entre mayúsculas y minúsculas.

Para ejecutar la acción **ImportarExportarTexto** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferText** del objeto **DoCmd**.

