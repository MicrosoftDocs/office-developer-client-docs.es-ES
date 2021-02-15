---
title: ImportarExportarDatos (acción de macro)
TOCTitle: ImportExportData macro action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e0cdf85461276d26005bc3066a387031a1086691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291890"
---
# <a name="importexportdata-macro-action"></a><span data-ttu-id="af34e-102">ImportarExportarDatos (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="af34e-102">ImportExportData macro action</span></span>

<span data-ttu-id="af34e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af34e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af34e-p101">La acción **ImportarExportarDatos** se utiliza para importar o exportar datos entre la base de datos de Access (.mdb o .accdb) o el proyecto de Access (.adp) actual y otra base de datos. Para bases de datos de Microsoft Access, también se puede vincular una tabla a la base de datos actual de Access desde otra base de datos. Con una tabla vinculada, se tiene acceso a los datos de la tabla mientras la propia tabla permanece en la otra base de datos.</span><span class="sxs-lookup"><span data-stu-id="af34e-p101">You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database. For Microsoft Access databases, you can also link a table to the current Access database from another database. With a linked table, you have access to the table's data while the table itself remains in the other database.</span></span>

> [!NOTE]
> <span data-ttu-id="af34e-107">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="af34e-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="af34e-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="af34e-108">Settings</span></span>

<span data-ttu-id="af34e-109">La acción **ImportarExportarDatos** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="af34e-109">The **ImportExportData** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af34e-110">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="af34e-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="af34e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="af34e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af34e-112"><strong>Tipo de transferencia</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-112"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p102">El tipo de transferencia que se desea realizar. Seleccione <strong>Importar</strong>, <strong>Exportar</strong> o <strong>Vincular</strong> en el cuadro <strong>Tipo de transferencia</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. La opción predeterminada es <strong>Importar</strong>.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p102">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p><p><span data-ttu-id="af34e-116"><strong>Nota</strong>: el tipo de transferencia <strong>Link</strong> no se admite en los proyectos de Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="af34e-116"><strong>NOTE</strong>: The <strong>Link</strong> transfer type is not supported for Access projects (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af34e-117"><strong>Tipo de base de datos</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-117"><strong>Database Type</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p103">El tipo de base de datos que se va a importar, exportar o vincular. Puede seleccionar <strong>Microsoft Access</strong> o alguno de los demás tipos de bases de datos del cuadro <strong>Tipo de base de datos</strong>. La opción predeterminada es <strong>Microsoft Access</strong>.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p103">The type of database to import from, export to, or link to. You can select <strong>Microsoft Access</strong> or one of a number of other database types in the <strong>Database Type</strong> box. The default is <strong>Microsoft Access</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af34e-121"><strong>Nombre de la base de datos</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-121"><strong>Database Name</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p104">El nombre de la base de datos desde la que realizar la importación, la exportación o la vinculación. Este argumento es necesario. Para los tipos de base de datos que usan archivos separados para cada tabla, como FoxPro, Paradox y dBASE, escriba el directorio que contiene el archivo. Escriba el nombre del archivo en el argumento <strong>Origen</strong> (importar o vincular) o el argumento <strong>Destino</strong> (exportar). Para las bases de datos de ODBC, escriba la cadena de conexión de conectividad abierta de bases de datos (ODBC) completa.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p104">The name of the database to import from, export to, or link to. Include the full path. This is a required argument. For types of databases that use separate files for each table, such as FoxPro, Paradox, and dBASE, enter the directory containing the file. Enter the file name in the <strong>Source</strong> argument (to import or link) or the <strong>Destination</strong> argument (to export). For ODBC databases, type the full Open Database Connectivity (ODBC) connection string.</span></span></p>
<p><span data-ttu-id="af34e-128">Para ver un ejemplo de una cadena de conexión, vincule una tabla externa a Access:</span><span class="sxs-lookup"><span data-stu-id="af34e-128">To see an example of a connection string, link an external table to Access:</span></span></p>
<ol>
<li><p><span data-ttu-id="af34e-129">En el cuadro de diálogo <strong>Obtener datos externos</strong>, escriba la ruta de acceso de la base de datos origen en el cuadro <strong>Nombre de archivo</strong>.</span><span class="sxs-lookup"><span data-stu-id="af34e-129">In the <strong>Get External Data</strong> dialog box, enter the path of your source database in the <strong>File name</strong> box.</span></span></p></li>
<li><p><span data-ttu-id="af34e-130">Haga clic en <strong>Vincular al origen de datos creando una tabla vinculada</strong> y luego en <strong>Aceptar</strong>.</span><span class="sxs-lookup"><span data-stu-id="af34e-130">Click <strong>Link to the data source by creating a linked table</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="af34e-131">Select a table in the <strong>Link Tables</strong> dialog box, and click <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="af34e-131">Select a table in the <strong>Link Tables</strong> dialog box, and click <strong>OK</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="af34e-p105">Abra la tabla recién vinculada en la vista Diseño y examine las propiedades de la tabla; para ello, haga clic en <strong>Hoja de propiedades</strong>, en la ficha <strong>Diseño</strong>, <strong>Herramientas</strong>. El texto de la propiedad <strong>Descripción</strong> es la cadena de conexión para esta tabla.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p105">Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>. The text in the <strong>Description</strong> property setting is the connection string for this table.</span></span></p>
<p><span data-ttu-id="af34e-134">Para obtener más información acerca de las cadenas de conexión ODBC, vea el archivo de Ayuda u otra documentación para el controlador ODBC de este tipo de base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="af34e-134">For more information about ODBC connection strings, see the Help file or other documentation for the ODBC driver of this type of ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af34e-135"><strong>Tipo de objeto</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-135"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p106">El tipo del objeto que se va a importar o exportar. Si selecciona <strong>Microsoft Access</strong> para el argumento <strong>Tipo de base de datos</strong>, puede seleccionar <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong>. La opción predeterminada es <strong>Tabla</strong>. Si selecciona cualquier otro tipo de base de datos o elige <strong>Vincular</strong> en el cuadro <strong>Tipo de transferencia</strong>, este argumento no se tiene en cuenta. Si está exportando una consulta de selección a una base de datos de Acces, seleccione <strong>Tabla</strong> en este argumento para exportar el conjunto de resultados de la consulta y seleccione <strong>Consulta</strong> para exportar la consulta en sí. Si está exportando una consulta de selección a otro tipo de base de datos, este argumento no se tiene en cuenta y el conjunto de resultados de la consulta se exporta.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p106">The type of object to import or export. If you select <strong>Microsoft Access</strong> for the <strong>Database Type</strong> argument, you can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box. The default is <strong>Table</strong>. If you select any other type of database, or if you select <strong>Link</strong> in the <strong>Transfer Type</strong> box, this argument is ignored. If you are exporting a select query to an Access database, select <strong>Table</strong> in this argument to export the result set of the query, and select <strong>Query</strong> to export the query itself. If you are exporting a select query to another type of database, this argument is ignored and the result set of the query is exported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af34e-142"><strong>Origen</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-142"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p107">El nombre de la tabla, consulta de selección u objeto de Access que se desea importar, exportar o vincular. Para algunos tipos de bases de datos, tales como FoxPro, Paradox o dBASE, se trata de un nombre de archivo. Incluya la extensión del nombre de archivo (tal como .dbf) en el nombre del archivo. Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="af34e-p107">The name of the table, select query, or Access object that you want to import, export, or link. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af34e-147"><strong>Destino</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-147"><strong>Destination</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p108">El nombre de la tabla importada, exportada o vinculada, la consulta de selección o el objeto de Access de la base de datos de destino. Para algunos tipos de base de datos, como FoxPro, Paradox o dBASE, se trata de un nombre de archivo. Incluya la extensión del nombre de archivo (como .dbf) en el nombre de archivo. Es un argumento obligatorio. Si selecciona <strong>Importar</strong> en el argumento <strong>Tipo de transferencia</strong> y <strong>Tabla</strong> en el argumento <strong>Tipo de objeto</strong>, Access crea una nueva tabla que contiene los datos de la tabla importada. Si importa una tabla u otro objeto, Access agrega un número al nombre si está en conflicto con un nombre existente. Por ejemplo, si importa Empleados y ya existe, Access cambiará el nombre de la tabla o el otro objeto importado a Empleados1. Si exporta una base de datos de Access u otra base de datos, Access reemplazará automáticamente las tablas o los otros objetos existentes que tengan el mismo nombre.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p108">The name of the imported, exported, or linked table, select query, or Access object in the destination database. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument and <strong>Table</strong> in the <strong>Object Type</strong> argument, Access creates a new table containing the data in the imported table. If you import a table or other object, Access adds a number to the name if it conflicts with an existing name. For example, if you import Employees and Employees already exists, Access renames the imported table or other object Employees1. If you export to an Access database or another database, Access automatically replaces any existing table or other object that has the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af34e-156"><strong>Estructura solamente</strong></span><span class="sxs-lookup"><span data-stu-id="af34e-156"><strong>Structure Only</strong></span></span></p></td>
<td><p><span data-ttu-id="af34e-p109">Especifica si se debe importar o exportar sólo la estructura de una tabla de base de datos sin ninguno de sus datos. Seleccione <strong>Sí</strong> o <strong>No</strong>. La opción predeterminada es <strong>No</strong>.  </span><span class="sxs-lookup"><span data-stu-id="af34e-p109">Specifies whether to import or export only the structure of a database table without any of its data. Select <strong>Yes</strong> or <strong>No</strong>. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="af34e-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af34e-160">Remarks</span></span>

<span data-ttu-id="af34e-p110">Puede importar y exportar tablas entre Access y otros tipos de bases de datos. También puede exportar consultas de selección de Access a otros tipos de bases de datos. Access exporta el conjunto de resultados de la consulta en forma de tabla. Puede importar y exportar cualquier objeto de base de datos de Access si ambas bases de datos son bases de datos de Access.</span><span class="sxs-lookup"><span data-stu-id="af34e-p110">You can import and export tables between Access and other types of databases. You can also export Access select queries to other types of databases. Access exports the result set of the query in the form of a table. You can import and export any Access database object if both databases are Access databases.</span></span>

<span data-ttu-id="af34e-p111">Si importa una tabla de otra base de datos de Access (.mdb o .accdb) que esté vinculada en esa base de datos, seguirá vinculada después de que la importe. Es decir, se importa el vínculo, no la propia tabla.</span><span class="sxs-lookup"><span data-stu-id="af34e-p111">If you import a table from another Access database (.mdb or .accdb) that's a linked table in that database, it will still be linked after you import it. That is, the link is imported, not the table itself.</span></span>

<span data-ttu-id="af34e-p112">Si la base de datos a la que desea obtener acceso requiere una contraseña, aparecerá un cuadro de diálogo cuando ejecute la macro. Escriba la contraseña en ese cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="af34e-p112">If the database you're accessing requires a password, a dialog box appears when you run the macro. Type the password in this dialog box.</span></span>

<span data-ttu-id="af34e-p113">La acción **ImportarExportarDatos** es similar a los comandos de la ficha **Datos externos**, en **Importar** o **Exportar**. Estos comandos se utilizan para seleccionar un origen de datos como, por ejemplo, una base de datos de Access u otro tipo, una hoja de cálculo o un archivo de texto. Si selecciona una base de datos, aparecerán uno o más cuadros de diálogo en los que podrá seleccionar el tipo de objeto que desea importar o exportar (para bases de datos de Access), el nombre del objeto y otras opciones, según la base de datos de la que vaya a importar o a la que vaya a exportar o vincular. Los argumentos de la acción **ImportarExportarDatos** reflejan las opciones de estos cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="af34e-p113">The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**. You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file. If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to. The arguments for the **ImportExportData** action reflect the options in these dialog boxes.</span></span>

<span data-ttu-id="af34e-173">Si desea suministrar información de índices para una tabla vinculada de dBASE, primero vincule la tabla:</span><span class="sxs-lookup"><span data-stu-id="af34e-173">If you want to supply index information for a linked dBASE table, first link the table:</span></span>

1.  <span data-ttu-id="af34e-174">Haga clic en **Archivo dBASE**.</span><span class="sxs-lookup"><span data-stu-id="af34e-174">Click **dBASE File**.</span></span>

2.  <span data-ttu-id="af34e-175">En el cuadro de diálogo **Obtener datos externos**, escriba la ruta de acceso del archivo de dBASE en el cuadro **Nombre de archivo**.</span><span class="sxs-lookup"><span data-stu-id="af34e-175">In the **Get External Data** dialog box, enter the path for the dBASE file in the **File name** box.</span></span>

3.  <span data-ttu-id="af34e-176">Haga clic en **Vincular al origen de datos creando una tabla vinculada** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="af34e-176">Click **Link to the data source by creating a linked table**, then click **OK**.</span></span>

4.  <span data-ttu-id="af34e-p114">Especifique los índices en los cuadros de diálogo para este comando. Access almacena la información de los índices en un archivo de información especial (.inf), ubicado en la carpeta de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="af34e-p114">Specify the indexes in the dialog boxes for this command. Access stores the index information in a special information (.inf) file, located in the Microsoft Office folder.</span></span>

5.  <span data-ttu-id="af34e-179">Luego, puede eliminar el vínculo a la tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="af34e-179">You can then delete the link to the linked table.</span></span>

<span data-ttu-id="af34e-180">La siguiente vez que utilice la acción **ImportarExportarDatos** para vincular esta tabla de dBASE, Access usará la información de índice especificada.</span><span class="sxs-lookup"><span data-stu-id="af34e-180">The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.</span></span>

> [!NOTE]
> <span data-ttu-id="af34e-181">[!NOTA] Si consulta o filtra una tabla vinculada, la consulta o el filtro distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="af34e-181">If you query or filter a linked table, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="af34e-182">Para ejecutar la acción **ImportarExportarDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferDatabase** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="af34e-182">To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.</span></span>

