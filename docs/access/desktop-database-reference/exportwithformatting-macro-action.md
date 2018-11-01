---
title: ExportarConFormato (acción de macro)
TOCTitle: ExportWithFormatting Macro Action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8a0ca9d2dde2ae5d39fb9159655f37b5140eee3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868024"
---
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="716c8-102">ExportarConFormato (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="716c8-102">ExportWithFormatting Macro Action</span></span>


<span data-ttu-id="716c8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="716c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="716c8-104">Puede usar la acción **ExportarConFormato** a fin de ejecutar la salida de los datos del objeto de base de datos de Microsoft Access especificado (una hoja de datos, un formulario, un informe, un módulo o una página de acceso a datos) en varios formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="716c8-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="716c8-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="716c8-105">Settings</span></span>

<span data-ttu-id="716c8-106">La acción **ExportarConFormato** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="716c8-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="716c8-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="716c8-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="716c8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="716c8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="716c8-109"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-p101">Tipo de objeto que contiene los datos a los que se va a dar salida. Haga clic en <strong>Tabla</strong> (para una hoja de datos de tabla), <strong>Consulta</strong> (para una hoja de datos de consulta), <strong>Formulario</strong> (para un formulario o una hoja de datos de formulario), <strong>Informe</strong>, <strong>Módulo</strong>, Página de acceso a datos, <strong>Vista de servidor</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. No puede dar salida a una macro. Si desea dar salida al objeto activo, seleccione su tipo con este argumento, pero deje en blanco el argumento <strong>Nombre del objeto</strong>. Este argumento es obligatorio. El valor predeterminado es <strong>Tabla</strong>.  </span><span class="sxs-lookup"><span data-stu-id="716c8-p101">The type of object containing the data to output. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't output a macro. If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank. This is a required argument. The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="716c8-116"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-p102">El nombre del objeto que contiene los datos de salida. El cuadro <strong>Nombre de objeto</strong> muestra todos los objetos de la base de datos del tipo seleccionado por el argumento <strong>Tipo de objeto</strong>. Si ejecuta una macro que contenga la acción <strong>ExportWithFormatting</strong> en una base de datos de biblioteca, Access busca primero el objeto con este nombre en la base de datos de biblioteca y, luego, en la base de datos actual.  </span><span class="sxs-lookup"><span data-stu-id="716c8-p102">The name of the object containing the data to output. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="716c8-120"><strong>Formato de resultados</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-121">Tipo de formato que se desea usar para dar salida a los datos.</span><span class="sxs-lookup"><span data-stu-id="716c8-121">The type of format you want to use to output the data.</span></span> <span data-ttu-id="716c8-122">Puede seleccionar <strong>libro de Excel 97 - Excel 2003 (*.xls)</strong>, <strong>Libro binario de Excel (*.xlsb)</strong>, <strong>Libro de Excel (*.xlsx)</strong>, <strong>HTML (*.htm; \* .html)</strong>, <strong>Libro de Microsoft Excel 5.0/95 (*.xls)</strong>, <strong>Formato PDF (*.pdf)</strong>, <strong> Formato de texto enriquecido (*.rtf)</strong>, <strong>archivos de texto (*.txt)</strong>o <strong>formato XPS (\*.xps)</strong>.</span><span class="sxs-lookup"><span data-stu-id="716c8-122">You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>.</span></span> <span data-ttu-id="716c8-123">Si deja este argumento en blanco, Access le preguntará por el formato de los resultados.</span><span class="sxs-lookup"><span data-stu-id="716c8-123">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="716c8-124"><strong>Archivo de salida</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-p104">Archivo en el que se va a dar salida a los datos, incluida la ruta de acceso completa. Puede incluir la extensión de nombre de archivo estándar para el formato que seleccione en el argumento <strong>Formato de resultados</strong>, pero no es necesario. Si deja en blanco el argumento <strong>Archivo de salida</strong>, Access pedirá el nombre de un archivo de salida.  </span><span class="sxs-lookup"><span data-stu-id="716c8-p104">The file to which you want to output the data, including the full path. You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required. If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="716c8-128"><strong>Autoinicio</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-129">Especifica si el software apropiado va a iniciarse inmediatamente después de ejecutarse la acción <strong>ExportarConFormato</strong>, con el archivo especificado por el argumento <strong>Archivo de salida</strong> abierto.</span><span class="sxs-lookup"><span data-stu-id="716c8-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="716c8-130"><strong>Archivo de plantilla</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-p105">Ruta de acceso y nombre de un archivo que se va a utilizar como plantilla para los archivos HTML. El archivo de plantilla es un archivo de texto que incluye etiquetas y símbolos HTML que son únicos para Access.</span><span class="sxs-lookup"><span data-stu-id="716c8-p105">The path and file name of a file you want to use as a template for HTML files. The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="716c8-133"><strong>Codificación</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-p106">Tipo de formato de codificación de caracteres que se va a utilizar para mostrar los datos de texto o HTML. Puede seleccionar <strong>MS-DOS</strong>, <strong>Unicode</strong> o <strong>Unicode (UTF-8)</strong>. La configuración del argumento <strong>MS-DOS</strong> sólo está disponible para los archivos de texto. Si deja este argumento en blanco, Access dará salida a los datos mediante la codificación predeterminada de Windows en el caso de los archivos de texto y mediante la codificación predeterminada del sistema en el caso de los archivos HTML.  </span><span class="sxs-lookup"><span data-stu-id="716c8-p106">The type of character encoding format you want used to output the text or HTML data. You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>. The <strong>MS-DOS</strong> argument setting is available only for text files. If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="716c8-138"><strong>Calidad de salida</strong></span><span class="sxs-lookup"><span data-stu-id="716c8-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="716c8-139">Seleccione <strong>Imprimir</strong> para optimizar el resultado de la impresión, o <strong>Pantalla</strong> para optimizar el resultado de la presentación en pantalla.</span><span class="sxs-lookup"><span data-stu-id="716c8-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="716c8-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="716c8-140">Remarks</span></span>

<span data-ttu-id="716c8-p107">Los datos de Access salen en el formato seleccionado y se puede leer con cualquier programa que utiliza el mismo formato. Por ejemplo, puede realizar la salida de un informe de Access con formato de documento con Formato de texto enriquecido y abrir el documento en Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="716c8-p107">The Access data is output in the selected format and can be read by any program that uses the same format. For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="716c8-p108">Si representa el objeto de base de datos con formato HTML, Access crea un archivo en formato HTML que contiene los datos del objeto. Puede usar el argumento **Archivo de plantilla** para especificar el archivo que debe utilizarse como plantilla del archivo .html.</span><span class="sxs-lookup"><span data-stu-id="716c8-p108">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object. You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="716c8-145">Se aplican las reglas siguientes cuando se utiliza la acción **ExportarConFormato** para dar salida a un objeto de base de datos en cualquiera de los formatos de salida:</span><span class="sxs-lookup"><span data-stu-id="716c8-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="716c8-p109">Los datos se pueden presentar en hojas de datos de tabla, consulta y formulario. En el archivo de salida, todos los campos de la hoja de datos tienen la misma apariencia que en Access, excepto los campos que contienen objetos OLE. Las columnas de los campos de objeto OLE se incluyen en el archivo de salida, pero los campos están en blanco.</span><span class="sxs-lookup"><span data-stu-id="716c8-p109">You can output data in table, query, and form datasheets. In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects. The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="716c8-149">Para un control que está enlazado a un campo Sí/No (un botón de alternar, botón de opción o casilla de verificación), el archivo de salida muestra el valor – 1 (Sí) o 0 (No).</span><span class="sxs-lookup"><span data-stu-id="716c8-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="716c8-150">En el caso de un cuadro de texto dependiente de un campo Hipervínculo, el archivo de salida muestra el hipervínculo para todos los formatos de salida, excepto el de texto MS-DOS (en este caso, el hipervínculo se muestra como texto normal).</span><span class="sxs-lookup"><span data-stu-id="716c8-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="716c8-151">Si se presentan los datos de un formulario en la vista Formulario, el archivo de salida siempre contiene la vista Hoja de datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="716c8-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="716c8-p110">Cuando se presenta una hoja de datos, un formulario o una página de acceso a datos en formato HTML, se crea un archivo .html. Cuando se presenta un informe en formato HTML, se crea un archivo .html por cada página del informe.</span><span class="sxs-lookup"><span data-stu-id="716c8-p110">When you output a datasheet, form, or data access page in HTML format, one .html file is created. When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="716c8-154">El resultado de ejecutar la acción **ExportarConFormato** es similar a hacer clic en una de las opciones del grupo **Exportar**, en la ficha **Datos externos**. Los argumentos de la acción se corresponden con los valores configurados en el cuadro de diálogo **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="716c8-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="716c8-155">Para ejecutar la acción **ExportarConFormato** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OutputTo** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="716c8-155">To run the **ExportWithFormatting** action in a Visual Basic for Applications (VBA) module, use the **OutputTo** method of the **DoCmd** object.</span></span>

