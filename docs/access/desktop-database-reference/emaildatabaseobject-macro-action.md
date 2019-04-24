---
title: EnviarPorCorreoObjetoDeBaseDeDatos (acción de macro)
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 15cb7d6c422a9d7b0fae17ab649b6cfbc1b497a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293570"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="aa065-102">EnviarPorCorreoObjetoDeBaseDeDatos (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="aa065-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="aa065-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa065-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="aa065-104">La acción **EnviarPorCorreoObjetoDeBaseDeDatos** se utiliza para incluir un objeto hoja de datos, formulario, informe, módulo o página de acceso a datos especificado de Microsoft Access en un mensaje de correo electrónico, desde donde se puede examinar y enviar.</span><span class="sxs-lookup"><span data-stu-id="aa065-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="aa065-105">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="aa065-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="aa065-106">Settings</span><span class="sxs-lookup"><span data-stu-id="aa065-106">Settings</span></span>

<span data-ttu-id="aa065-107">La acción **EnviarPorCorreoObjetoDeBaseDeDatos** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="aa065-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa065-108">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="aa065-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="aa065-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa065-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa065-110"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p101">El tipo de objeto que se va a incluir en el mensaje de correo. Haga clic en <strong>Tabla</strong> (en el caso de una hoja de datos de tabla), <strong>Consulta</strong> (si es una hoja de datos de una consulta), <strong>Formulario</strong> (para un formulario u hoja de datos de un formulario), <strong>Informe</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. No es posible enviar una macro. Si desea incluir el objeto activo, seleccione su tipo con este argumento, pero deje en blanco el argumento <strong>Nombre del objeto</strong>.  </span><span class="sxs-lookup"><span data-stu-id="aa065-p101">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa065-115"><strong>Nombre del objeto</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p102">El nombre del objeto que se va a incluir en el mensaje de correo. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong> que existen en la base de datos. Si deja ambos argumentos ( <strong>Tipo de objeto</strong> y <strong>Nombre del objeto</strong> ) en blanco, Access envía a la aplicación de correo un mensaje sin ningún objeto de base de datos. Si ejecuta una macro que contiene la acción <strong>EMailDatabaseObject</strong> en una base de datos de biblioteca, Acceso busca el objeto con ese nombre primero en la base de datos de biblioteca y después en la base de datos actual.  </span><span class="sxs-lookup"><span data-stu-id="aa065-p102">The name of the object to include in the mail message. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object. If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa065-120"><strong>Formato de resultados</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-121">El tipo de formato que desea usar para el objeto incluido.</span><span class="sxs-lookup"><span data-stu-id="aa065-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="aa065-122">La lista de formatos que puede seleccionar variará en función de lo que seleccione para el argumento <strong>tipo de objeto</strong> .</span><span class="sxs-lookup"><span data-stu-id="aa065-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="aa065-123">Los formatos disponibles pueden <strong>incluir excel 97-excel 2003 libro (*. xls)</strong>, <strong>libro binario de Excel (*. xlsb)</strong>, <strong>libro de Excel (*. xlsx)</strong>, <strong>HTML (*. htm, *. html)</strong>, <strong>libro de Microsoft Excel 5.0/95 (*. xls)</strong>, <strong>formato PDF </strong>, <strong>Fomat de texto enriquecido (*. rtf)</strong>, <strong>archivos de texto (*. txt)</strong>o <strong>formato XPS (\*. XPS)</strong>.</span><span class="sxs-lookup"><span data-stu-id="aa065-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="aa065-124">en el cuadro <strong>formato de salida</strong> .</span><span class="sxs-lookup"><span data-stu-id="aa065-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="aa065-125">Los módulos solo se pueden enviar en formato de texto.</span><span class="sxs-lookup"><span data-stu-id="aa065-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="aa065-126">Las páginas de acceso a datos solo se pueden enviar en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="aa065-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="aa065-127">Si deja este argumento en blanco, Access le preguntará por el formato de los resultados.</span><span class="sxs-lookup"><span data-stu-id="aa065-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa065-128"><strong>Para</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p104">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.  </span><span class="sxs-lookup"><span data-stu-id="aa065-p104">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa065-133"><strong>CC</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-134">Destinatarios del mensaje cuyos nombres desee indicar en la línea <strong>CC</strong> (&quot;copia&quot;carbón) del mensaje de correo.</span><span class="sxs-lookup"><span data-stu-id="aa065-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="aa065-135">Si deja en blanco este argumento, la línea <strong>CC</strong> del mensaje de correo queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="aa065-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa065-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-137">Destinatarios del mensaje cuyos nombres desee indicar en la línea <strong>CCO</strong> (&quot;copia&quot;carbón oculta) del mensaje de correo.</span><span class="sxs-lookup"><span data-stu-id="aa065-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="aa065-138">Si deja en blanco este argumento, la línea <strong>CCO</strong> del mensaje de correo queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="aa065-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa065-139"><strong>Asunto</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p107">Asunto al que se refiere el mensaje. Este texto aparecerá en la línea <strong>Asunto</strong> del mensaje. Si deja en blanco este argumento, la línea <strong>Asunto</strong> del mensaje de correo queda en blanco.  </span><span class="sxs-lookup"><span data-stu-id="aa065-p107">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa065-143"><strong>Texto del mensaje</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p108">Cualquier texto que desee incluir en el mensaje además del objeto de base de datos. Este texto aparecerá en el cuerpo principal del mensaje, después del objeto. Si deja este argumento en blanco, no se incluirá ningún texto. Si ha dejado los argumentos <strong>Tipo de objeto</strong> y <strong>Nombre del objeto</strong> en blanco, puede utilizar este argumento para enviar un mensaje de correo sin ningún objeto de base de datos.  </span><span class="sxs-lookup"><span data-stu-id="aa065-p108">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa065-148"><strong>Modificar el mensaje</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p109">Especifica si el mensaje se puede modificar o no antes de enviarlo. Si selecciona <strong>Sí</strong>, la aplicación de correo electrónico se iniciará automáticamente y el mensaje podrá ser modificado. Si selecciona <strong>No</strong>, el mensaje se enviará sin dar opción a modificarlo. El valor predeterminado es <strong>Sí</strong>.  </span><span class="sxs-lookup"><span data-stu-id="aa065-p109">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa065-153"><strong>Archivo de plantilla</strong></span><span class="sxs-lookup"><span data-stu-id="aa065-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="aa065-p110">La ruta de acceso y el nombre de un archivo que se desea utilizar como plantilla para un archivo HTML. El archivo de plantilla es un archivo que contiene etiquetas HTML.</span><span class="sxs-lookup"><span data-stu-id="aa065-p110">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aa065-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa065-156">Remarks</span></span>

<span data-ttu-id="aa065-p111">El objeto incluido en el mensaje de correo se encuentra en el formato especificado. Al hacer doble clic sobre el objeto, éste se abrirá con el software correspondiente.</span><span class="sxs-lookup"><span data-stu-id="aa065-p111">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="aa065-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span><span class="sxs-lookup"><span data-stu-id="aa065-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="aa065-p112">Puede enviar hojas de datos de tabla, consulta y formulario. En el objeto incluido, todos los campos de la hoja de datos tienen la misma apariencia que en Access, excepto los campos que contengan objetos OLE. Las columnas de estos campos se incluyen en el objeto, pero los campos están en blanco.</span><span class="sxs-lookup"><span data-stu-id="aa065-p112">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="aa065-163">Para un control dependiente de un campo Sí/No (botón de alternancia, botón de opción o casilla de verificación), el archivo de salida muestra el valor –1 (Sí) o 0 (No).</span><span class="sxs-lookup"><span data-stu-id="aa065-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="aa065-164">Para un cuadro de texto dependiente de un campo Hipervínculo, el archivo de salida muestra el hipervínculo para todos los formatos de salida excepto texto MS-DOS (en este caso, el hipervínculo se muestra como texto normal).</span><span class="sxs-lookup"><span data-stu-id="aa065-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="aa065-165">Si se envía un formulario en la vista Formulario, el objeto incluido siempre contiene la vista Hoja de datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="aa065-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="aa065-p113">Si envía un informe, los únicos controles que se incluirán en el archivo serán cuadros de texto y (en algunos casos) etiquetas. El resto de los controles se omiten. Tampoco se incluye la información del encabezado y el pie de página. La única excepción a esto es que, al enviar un informe en formato Excel, se incluirá un cuadro de texto en un pie de grupo que contenga una expresión con la función **Suma**. El objeto no incluirá ningún otro control del encabezado o pie de página (ni ninguna función de agregado distinta de **Suma**).</span><span class="sxs-lookup"><span data-stu-id="aa065-p113">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="aa065-171">Los subinformes se incluyen en el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa065-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="aa065-p114">Si se envía una hoja de datos, formulario o página de acceso a datos en formato HTML, se crea un archivo .html. Si se envía un informe en formato HTML, se crea un archivo .html para cada página del informe.</span><span class="sxs-lookup"><span data-stu-id="aa065-p114">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="aa065-174">Para ejecutar la acción **EnviarPorCorreoObjetoDeBaseDeDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **SendObject** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="aa065-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="aa065-175">Sobre el colaborador</span><span class="sxs-lookup"><span data-stu-id="aa065-175">About the contributor</span></span>

<span data-ttu-id="aa065-176">**Vínculo proporcionado por** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), fundador y Presidente de FMS, Inc., un proveedor líder de soluciones de bases de datos personalizadas y herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="aa065-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="aa065-177">Características y límites del uso del método EnviarObjeto para enviar correos</span><span class="sxs-lookup"><span data-stu-id="aa065-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





