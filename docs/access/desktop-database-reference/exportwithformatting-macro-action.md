---
title: ExportarConFormato (acción de macro)
TOCTitle: ExportWithFormatting macro action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ae03262489b707257a4aee93e4380aa70329856a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924438"
---
# <a name="exportwithformatting-macro-action"></a>ExportarConFormato (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **ExportarConFormato** a fin de ejecutar la salida de los datos del objeto de base de datos de Microsoft Access especificado (una hoja de datos, un formulario, un informe, un módulo o una página de acceso a datos) en varios formatos de salida.

## <a name="settings"></a>Configuración

La acción **ExportarConFormato** tiene los siguientes argumentos.

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
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>Tipo de objeto que contiene los datos a los que se va a dar salida. Haga clic en <strong>Tabla</strong> (para una hoja de datos de tabla), <strong>Consulta</strong> (para una hoja de datos de consulta), <strong>Formulario</strong> (para un formulario o una hoja de datos de formulario), <strong>Informe</strong>, <strong>Módulo</strong>, Página de acceso a datos, <strong>Vista de servidor</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. No puede dar salida a una macro. Si desea dar salida al objeto activo, seleccione su tipo con este argumento, pero deje en blanco el argumento <strong>Nombre del objeto</strong>. Este argumento es obligatorio. El valor predeterminado es <strong>Tabla</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>El nombre del objeto que contiene los datos de salida. El cuadro <strong>Nombre de objeto</strong> muestra todos los objetos de la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si ejecuta una macro que contenga la acción <strong>ExportWithFormatting</strong> en una base de datos de biblioteca, Access busca primero el objeto con este nombre en la base de datos de biblioteca y, luego, en la base de datos actual.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Formato de resultados</strong></p></td>
<td><p>Tipo de formato que se desea usar para dar salida a los datos. Puede seleccionar <strong>libro de Excel 97 - Excel 2003 (*.xls)</strong>, <strong>Libro binario de Excel (*.xlsb)</strong>, <strong>Libro de Excel (*.xlsx)</strong>, <strong>HTML (*.htm; * .html)</strong>, <strong>Libro de Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Formato PDF (*.pdf)</strong>, <strong> Formato de texto enriquecido (*.rtf)</strong>, <strong>archivos de texto (*.txt)</strong>o <strong>formato XPS (*.xps)</strong>. Si deja este argumento en blanco, Access le preguntará por el formato de los resultados.</p></td>
</tr>
<tr class="even">
<td><p><strong>Archivo de salida</strong></p></td>
<td><p>Archivo en el que se va a dar salida a los datos, incluida la ruta de acceso completa. Puede incluir la extensión de nombre de archivo estándar para el formato que seleccione en el argumento <strong>Formato de resultados</strong>, pero no es necesario. Si deja en blanco el argumento <strong>Archivo de salida</strong>, Access pedirá el nombre de un archivo de salida.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Autoinicio</strong></p></td>
<td><p>Especifica si el software apropiado va a iniciarse inmediatamente después de ejecutarse la acción <strong>ExportarConFormato</strong>, con el archivo especificado por el argumento <strong>Archivo de salida</strong> abierto.</p></td>
</tr>
<tr class="even">
<td><p><strong>Archivo de plantilla</strong></p></td>
<td><p>Ruta de acceso y nombre de un archivo que se va a utilizar como plantilla para los archivos HTML. El archivo de plantilla es un archivo de texto que incluye etiquetas y símbolos HTML que son únicos para Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Codificación</strong></p></td>
<td><p>Tipo de formato de codificación de caracteres que se va a utilizar para mostrar los datos de texto o HTML. Puede seleccionar <strong>MS-DOS</strong>, <strong>Unicode</strong> o <strong>Unicode (UTF-8)</strong>. La configuración del argumento <strong>MS-DOS</strong> sólo está disponible para los archivos de texto. Si deja este argumento en blanco, Access dará salida a los datos mediante la codificación predeterminada de Windows en el caso de los archivos de texto y mediante la codificación predeterminada del sistema en el caso de los archivos HTML.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Calidad de salida</strong></p></td>
<td><p>Seleccione <strong>Imprimir</strong> para optimizar el resultado de la impresión, o <strong>Pantalla</strong> para optimizar el resultado de la presentación en pantalla.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Los datos de Access salen en el formato seleccionado y se puede leer con cualquier programa que utiliza el mismo formato. Por ejemplo, puede realizar la salida de un informe de Access con formato de documento con Formato de texto enriquecido y abrir el documento en Microsoft Word.

Si representa el objeto de base de datos con formato HTML, Access crea un archivo en formato HTML que contiene los datos del objeto. Puede usar el argumento **Archivo de plantilla** para especificar el archivo que debe utilizarse como plantilla del archivo .html.

Se aplican las reglas siguientes cuando se utiliza la acción **ExportarConFormato** para dar salida a un objeto de base de datos en cualquiera de los formatos de salida:

  - Los datos se pueden presentar en hojas de datos de tabla, consulta y formulario. En el archivo de salida, todos los campos de la hoja de datos tienen la misma apariencia que en Access, excepto los campos que contienen objetos OLE. Las columnas de los campos de objeto OLE se incluyen en el archivo de salida, pero los campos están en blanco.

  - Para un control que está enlazado a un campo Sí/No (un botón de alternar, botón de opción o casilla de verificación), el archivo de salida muestra el valor – 1 (Sí) o 0 (No).

  - En el caso de un cuadro de texto dependiente de un campo Hipervínculo, el archivo de salida muestra el hipervínculo para todos los formatos de salida, excepto el de texto MS-DOS (en este caso, el hipervínculo se muestra como texto normal).

  - Si se presentan los datos de un formulario en la vista Formulario, el archivo de salida siempre contiene la vista Hoja de datos del formulario.

  - Cuando se presenta una hoja de datos, un formulario o una página de acceso a datos en formato HTML, se crea un archivo .html. Cuando se presenta un informe en formato HTML, se crea un archivo .html por cada página del informe.

El resultado de ejecutar la acción **ExportarConFormato** es similar a hacer clic en una de las opciones del grupo **Exportar**, en la ficha **Datos externos**. Los argumentos de la acción se corresponden con los valores configurados en el cuadro de diálogo **Exportar**.

Para ejecutar la acción **ExportarConFormato** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OutputTo** del objeto **DoCmd**.

