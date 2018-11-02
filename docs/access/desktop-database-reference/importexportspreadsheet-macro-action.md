---
title: ImportarExportarHojaDeCálculo (acción de macro)
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d630602d7b81fe44427d892d62275f4509dbdc2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923976"
---
# <a name="importexportspreadsheet-macro-action"></a><span data-ttu-id="a4ee8-102">ImportarExportarHojaDeCálculo (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a4ee8-102">ImportExportSpreadsheet macro action</span></span>


<span data-ttu-id="a4ee8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4ee8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4ee8-p101">Puede usar la acción **ImportarExportarHojaDeCálculo** para importar o exportar datos entre la base de datos de Access activa (.mdb o .accdb) o un proyecto de Access (.adp) y un archivo de hoja de cálculo. También puede vincular los datos en una hoja de cálculo de Microsoft Excel a la base de datos de Microsoft Access. Con una hoja de cálculo vinculada, puede ver y editar los datos de la hoja de cálculo con Access y a su vez tener un acceso total a los datos desde el programa de hoja de cálculo Excel. También puede vincular a datos en un archivo de hoja de cálculo de Lotus 1-2-3, pero estos datos son de solo lectura en Access.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p101">You can use the **ImportExportSpreadsheet** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and a spreadsheet file. You can also link the data in a Microsoft Excel spreadsheet to the current Microsoft Access database. With a linked spreadsheet, you can view and edit the spreadsheet data with Access while still allowing complete access to the data from your Excel spreadsheet program. You can also link to data in a Lotus 1-2-3 spreadsheet file, but this data is read-only in Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a4ee8-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="a4ee8-110">Configuración</span><span class="sxs-lookup"><span data-stu-id="a4ee8-110">Setting</span></span>

<span data-ttu-id="a4ee8-111">La acción **TransferirHojaCálculo** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-111">The **TransferSpreadsheet** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4ee8-112">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="a4ee8-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a4ee8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4ee8-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4ee8-114"><strong>Tipo de transferencia</strong></span><span class="sxs-lookup"><span data-stu-id="a4ee8-114"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a4ee8-p103">El tipo de transferencia que se desea realizar. Seleccione <strong>Importar</strong>, <strong>Exportar</strong> o <strong>Vincular</strong> en el cuadro <strong>Tipo de transferencia</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. La opción predeterminada es <strong>Importar</strong>.  </span><span class="sxs-lookup"><span data-stu-id="a4ee8-p103">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="a4ee8-118">Los proyectos de Access (.adp) no admiten el tipo de transferencia <STRONG>Vincular</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-118">The <STRONG>Link</STRONG> transfer type is not supported for Access projects (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4ee8-119"><strong>Tipo de hoja de cálculo</strong></span><span class="sxs-lookup"><span data-stu-id="a4ee8-119"><strong>Spreadsheet Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a4ee8-p104">El tipo de hoja de cálculo que se va a importar, exportar o vincular. Puede seleccionar uno entre varios tipos de hojas de cálculo en el cuadro. El valor predeterminado es <strong>Libro de Excel</strong>.  </span><span class="sxs-lookup"><span data-stu-id="a4ee8-p104">The type of spreadsheet to import from, export to, or link to. You can select one of a number of spreadsheet types in the box. The default is <strong>Excel Workbook</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="a4ee8-p105">Puede importar desde y vincular (solo lectura) a archivos .WK4 de Lotus, pero no puede exportar datos de Access a este formato de hoja de cálculo. Con esta acción, Access tampoco admite ya importar, exportar o vincular datos de hojas de cálculo .WKS de Lotus o Excel versión 2.0. Si desea importar o vincular datos de hojas de cálculo en formato Excel versión 2.0 o .WKS de Lotus, convierta los datos de las hojas de cálculo a una versión posterior de Excel o de Lotus 1-2-3 antes de importar o vincular los datos con Access.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p105">You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format. Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action. If you want to import from or link to spreadsheet data in Excel version 2.0 or Lotus .WKS format, convert the spreadsheet data to a later version of Excel or Lotus 1-2-3 before importing or linking the data into Access.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4ee8-126"><strong>Nombre de la tabla</strong></span><span class="sxs-lookup"><span data-stu-id="a4ee8-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a4ee8-p106">El nombre de la tabla de Access a la que importar los datos de la hoja de cálculo, desde la que exportar los datos de la hoja de cálculo, o a la que vincular los datos de la hoja de cálculo. También puede escribir el nombre de la consulta de selección de Access desde la que quiera exportar los datos. Se trata de un argumento obligatorio. Si selecciona <strong>Importar</strong> en el argumento <strong>Tipo de transferencia</strong>, Access anexa los datos de la hoja de cálculo a esta tabla, si existe. De lo contrario, Access crea una nueva tabla que contiene los datos de la hoja de cálculo. En Access, no puede usar una instrucción SQL para especificar los datos para exportar al usar la acción <strong>ImportarExportarHojaDeCálculo</strong>. En lugar de usar una instrucción SQL, debe crear primero una consulta y, luego, especificar el nombre de la consulta en el argumento <strong>Nombre de tabla</strong>.  </span><span class="sxs-lookup"><span data-stu-id="a4ee8-p106">The name of the Access table to import spreadsheet data to, export spreadsheet data from, or link spreadsheet data to. You can also type the name of the Access select query you want to export data from. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument, Access appends the spreadsheet data to this table if the table already exists. Otherwise, Access creates a new table containing the spreadsheet data. In Access, you can't use an SQL statement to specify data to export when you are using the <strong>ImportExportSpreadsheet</strong> action. Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4ee8-134"><strong>Nombre del archivo</strong></span><span class="sxs-lookup"><span data-stu-id="a4ee8-134"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a4ee8-p107">El nombre del archivo de la hoja de cálculo desde la que importar, exportar o vincular. Incluir la ruta de acceso completa. Se trata de un argumento obligatorio. Access crea una nueva hoja de cálculo al exportar datos desde Access. Si el nombre del archivo es el mismo que el nombre de una hoja de cálculo existente, Access reemplaza la hoja de cálculo existente, a menos que exporte a un libro de Excel versión 5.0 o posterior. En este caso, Access copia los datos exportados a la siguiente nueva hoja de cálculo disponible del libro. Si importa desde o vincula a una hoja de cálculo de Excel versión 5.0 o posterior, puede especificar una hoja cálculo concreta con el argumento <strong>Rango</strong>.  </span><span class="sxs-lookup"><span data-stu-id="a4ee8-p107">The name of the spreadsheet file to import from, export to, or link to. Include the full path. This is a required argument. Access creates a new spreadsheet when you export data from Access. If the file name is the same as the name of an existing spreadsheet, Access replaces the existing spreadsheet, unless you're exporting to an Excel version 5.0 or later workbook. In that case, Access copies the exported data to the next available new worksheet in the workbook. If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can specify a particular worksheet by using the <strong>Range</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4ee8-142"><strong>Contiene nombres de campo</strong></span><span class="sxs-lookup"><span data-stu-id="a4ee8-142"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="a4ee8-p108">Especifica si la primera fila de la hoja de cálculo contiene los nombres de los campos. Si selecciona <strong>Sí</strong>, Access usa los nombres de esta fila como los nombres de campo en la tabla de Access al importar o vincular los datos de la hoja de cálculo. Si selecciona <strong>No</strong>, Access trata la primera fila como una fila de datos normal. El valor predeterminado es <strong>No</strong>. Al exportar una tabla de Access o al seleccionar una consulta para una hoja de cálculo, se insertan los nombres de campo en la primera fila de la hoja de cálculo, independientemente de lo que seleccione en este argumento.  </span><span class="sxs-lookup"><span data-stu-id="a4ee8-p108">Specifies whether the first row of the spreadsheet contains the names of the fields. If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the spreadsheet data. If you select <strong>No</strong>, Access treats the first row as a normal row of data. The default is <strong>No</strong>. When you export an Access table or select query to a spreadsheet, the field names are inserted into the first row of the spreadsheet no matter what you select in this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4ee8-148"><strong>Intervalo</strong></span><span class="sxs-lookup"><span data-stu-id="a4ee8-148"><strong>Range</strong></span></span></p></td>
<td><p><span data-ttu-id="a4ee8-p109">Rango de celdas que se van a importar o vincular. Deje este argumento en blanco para importar o vincular la hoja de cálculo completa. Puede escribir el nombre de un rango de la hoja de cálculo o especificar un rango de celdas para importar o vincular, tal como A1:E25 (observe que la sintaxis A1..E25 no funciona en Access 97 o en una versión posterior). Si importa o vincula con una hoja de cálculo de Excel versión 5.0 o posterior, puede anteponer al rango el nombre de la hoja de cálculo y un signo de exclamación (por ejemplo, Presupuesto!A1:C7).</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p109">The range of cells to import or link. Leave this argument blank to import or link the entire spreadsheet. You can type the name of a range in the spreadsheet or specify the range of cells to import or link, such as A1:E25 (note that the A1..E25 syntax does not work in Access 97 or later). If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can prefix the range with the name of the worksheet and an exclamation point; for example, Budget!A1:C7.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="a4ee8-p110">Cuando se exporta a una hoja de cálculo, debe dejar en blanco este argumento. Si especifica un rango, se producirá un error en la exportación.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p110">When you export to a spreadsheet, you must leave this argument blank. If you enter a range, the export will fail.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a4ee8-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4ee8-155">Remarks</span></span>

<span data-ttu-id="a4ee8-p111">Los datos de las consultas de selección de Access se pueden exportar a hojas de cálculo. Access exporta el conjunto de resultados de la consulta tratándolo como si fuera una tabla.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p111">You can export the data in Access select queries to spreadsheets. Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="a4ee8-158">Los datos de una hoja de cálculo que se anexan a una tabla de Access existente deben ser compatibles con la estructura de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-158">Spreadsheet data that you append to an existing Access table must be compatible with the table's structure.</span></span>

  - <span data-ttu-id="a4ee8-159">Cada campo de la hoja de cálculo debe contener el mismo tipo de datos que el campo correspondiente de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-159">Each field in the spreadsheet must be of the same data type as the corresponding field in the table.</span></span>

  - <span data-ttu-id="a4ee8-160">Los campos deben estar en el mismo orden (a menos que haya establecido el argumento **Contiene nombres de campo** en **Sí**, en cuyo caso los nombres de los campos de la hoja de cálculo deben coincidir con los nombres de los campos de la tabla).</span><span class="sxs-lookup"><span data-stu-id="a4ee8-160">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the spreadsheet must match the field names in the table).</span></span>

<span data-ttu-id="a4ee8-p112">Esta acción es similar a hacer clic en la pestaña **Datos externos** y hacer clic en **Excel** en el grupo **Importar** o **Exportar**, o bien, hacer clic en **Más** en el grupo **Importar** o **Exportar** y hacer clic en **Archivo de Lotus 1-2-3**. Estos comandos se usan para seleccionar un origen de datos, tal como Access o un tipo de base de datos, hoja de cálculo o archivo de texto. Si selecciona una hoja de cálculo, aparecerán una serie de cuadros de diálogo, o se ejecutará un asistente de Access, donde se puede seleccionar el nombre de la hoja de cálculo y otras opciones. Los argumentos de la acción **ImportarExportarHojaDeCálculo** reflejan las opciones de estos cuadros de diálogo o de los asistentes.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-p112">This action is similar to clicking the **External Data** tab and clicking **Excel** in the **Import** or **Export** group, or clicking **More** in the **Import** or **Export** group and clicking **Lotus 1-2-3 File**. You can use these commands to select a source of data, such as Access or a type of database, spreadsheet, or text file. If you select a spreadsheet, a series of dialog boxes appear, or an Access wizard runs, in which you select the name of the spreadsheet and other options. The arguments of the **ImportExportSpreadsheet** action reflect the options in these dialog boxes or in the wizards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a4ee8-165">[!NOTA] Si consulta o filtra una hoja de cálculo vinculada, la consulta o el filtro distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-165">If you query or filter a linked spreadsheet, the query or filter is case-sensitive.</span></span></P>



<span data-ttu-id="a4ee8-166">Si crea un vínculo a una hoja de cálculo de Excel que está abierta en modo Edición, Access esperará hasta que la hoja de cálculo de Excel salga del modo Edición antes de completar el vínculo. No existe un tiempo máximo para esta espera.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-166">If you link to an Excel spreadsheet that is open in Edit mode, Access will wait until the Excel spreadsheet is out of Edit mode before completing the link; there's no time-out.</span></span>

<span data-ttu-id="a4ee8-167">Para ejecutar la acción **ImportarExportarHojaDeCálculo** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferSpreadsheet** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="a4ee8-167">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>

