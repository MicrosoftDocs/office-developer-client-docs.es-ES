---
title: Inicialización del controlador de origen de datos de texto
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291424"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="9d00c-102">Inicialización del controlador de origen de datos de texto</span><span class="sxs-lookup"><span data-stu-id="9d00c-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="9d00c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d00c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d00c-104">El mismo controlador de base de datos se usa tanto para orígenes de datos de texto como para orígenes de datos HTML.</span><span class="sxs-lookup"><span data-stu-id="9d00c-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="9d00c-105">Al instalar el controlador de base de datos de origen de datos de texto, el programa de instalación escribe un conjunto de valores predeterminados en el Registro de Microsoft Windows en las subclaves Engines e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="9d00c-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="9d00c-106">No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d00c-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="9d00c-107">Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de orígenes de datos de texto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="9d00c-108">Configuración de inicialización del origen de datos de texto</span><span class="sxs-lookup"><span data-stu-id="9d00c-108">Text data source initialization settings</span></span>

<span data-ttu-id="9d00c-109">La **carpeta de texto de \\ formatos ISAM \\** del motor de conectividad de Access incluye la configuración de inicialización del controlador Acetxt.dll, que se usa para el acceso externo a los archivos de datos de texto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="9d00c-110">En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="9d00c-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

<span data-ttu-id="9d00c-111">El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Text de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d00c-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d00c-112">Entrada</span><span class="sxs-lookup"><span data-stu-id="9d00c-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="9d00c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d00c-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-114">win32</span><span class="sxs-lookup"><span data-stu-id="9d00c-114">win32</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p103">Ubicación de Acetxt.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p103">The location of Acetxt.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="9d00c-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p104">Número de filas que se van a examinar para estimar los tipos de columnas. Si se establece en 0, se analizará el archivo completo. El valor predeterminado es 25. Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p104">The number of rows to be scanned when guessing the column types. If set to 0, the entire file will be searched. The default is 25. Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="9d00c-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p105">Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p105">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="9d00c-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="9d00c-127">Indicador de cómo se almacenan las páginas de texto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="9d00c-128">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="9d00c-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="9d00c-129">ANSI, la página de códigos ANSI del equipo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="9d00c-130">Se realizan las conversiones AnsiToUnicode y UnicodeToAnsi.</span><span class="sxs-lookup"><span data-stu-id="9d00c-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="9d00c-131">OEM, la página de códigos OEM del equipo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="9d00c-132">Se realizan las conversiones OemToUnicode y UnicodeToOem.</span><span class="sxs-lookup"><span data-stu-id="9d00c-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="9d00c-133">Unicode, no se realizan las conversiones de página de códigos .</span><span class="sxs-lookup"><span data-stu-id="9d00c-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="9d00c-134">&lt;número &gt; decimal: número de página de códigos de un juego de caracteres específico.</span><span class="sxs-lookup"><span data-stu-id="9d00c-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="9d00c-135">Se realizan las conversiones a y desde Unicode.</span><span class="sxs-lookup"><span data-stu-id="9d00c-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="9d00c-136">El valor predeterminado es ANSI.</span><span class="sxs-lookup"><span data-stu-id="9d00c-136">The default is ANSI.</span></span> <span data-ttu-id="9d00c-137">Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="9d00c-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-138">Formato</span><span class="sxs-lookup"><span data-stu-id="9d00c-138">Format</span></span></p></td>
<td><p><span data-ttu-id="9d00c-139">Puede ser cualquiera de los siguientes: TabDelimited, CSVDelimited, Delimited ( &lt; single character &gt; ).</span><span class="sxs-lookup"><span data-stu-id="9d00c-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="9d00c-140">El delimitador de un solo carácter en el formato Delimitado puede ser cualquier carácter individual excepto una comilla doble ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="9d00c-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="9d00c-141">El valor predeterminado es CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="9d00c-141">The default is CSVDelimited.</span></span> <span data-ttu-id="9d00c-142">Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="9d00c-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-143">Extensiones</span><span class="sxs-lookup"><span data-stu-id="9d00c-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p112">Extensiones de los archivos que se van a examinar al buscar datos basados en texto. Las extensiones predeterminadas son txt, csv, tab, asc. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p112">The extension of any files to be browsed when looking for text-based data. The default is txt, csv, tab, asc. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="9d00c-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p113">Valor binario que indica si se incluye el símbolo de moneda adecuado al exportar campos de moneda. Un valor de 01 indica que se incluye el símbolo. Un valor de 00 indica que sólo se exportan los datos numéricos. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p113">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported. A value of 01 indicates that the symbol is included. A value of 00 indicates that only the numeric data is exported. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="9d00c-153">Formatos ISAM de origen de datos de texto</span><span class="sxs-lookup"><span data-stu-id="9d00c-153">Text data source ISAM formats</span></span>

<span data-ttu-id="9d00c-154">La **carpeta de texto de \\ formatos ISAM \\** del motor de conectividad de Access contiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="9d00c-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d00c-155">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="9d00c-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="9d00c-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d00c-156">Type</span></span></p></th>
<th><p><span data-ttu-id="9d00c-157">Valor</span><span class="sxs-lookup"><span data-stu-id="9d00c-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-158">Motor</span><span class="sxs-lookup"><span data-stu-id="9d00c-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="9d00c-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-160">Texto</span><span class="sxs-lookup"><span data-stu-id="9d00c-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="9d00c-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="9d00c-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-163">Archivos de texto (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="9d00c-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="9d00c-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="9d00c-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-166">Archivos de texto (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="9d00c-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="9d00c-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="9d00c-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-169">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="9d00c-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="9d00c-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-172">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="9d00c-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="9d00c-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9d00c-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="9d00c-175">2 </span><span class="sxs-lookup"><span data-stu-id="9d00c-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="9d00c-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="9d00c-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-178">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="9d00c-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-181">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="9d00c-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p114">Importar datos del archivo externo a la base de datos activa. Al cambiar datos en la base de datos activa, no cambiarán los del archivo externo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p114">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="9d00c-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="9d00c-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p115">Crear una tabla en la base de datos activa que está vinculada al archivo externo. Si se cambian datos en la base de datos activa, también cambiarán los del archivo externo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p115">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="9d00c-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p116">Exportar datos de la base de datos activa a un archivo de texto. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p116">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="9d00c-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="9d00c-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-196">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="9d00c-197">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="9d00c-198">Formatos ISAM de importación HTML</span><span class="sxs-lookup"><span data-stu-id="9d00c-198">HTML import ISAM formats</span></span>

<span data-ttu-id="9d00c-199">La **carpeta de importación HTML de \\ \\ formatos HTML** del motor de conectividad de Access contiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="9d00c-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d00c-200">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="9d00c-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="9d00c-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d00c-201">Type</span></span></p></th>
<th><p><span data-ttu-id="9d00c-202">Valor</span><span class="sxs-lookup"><span data-stu-id="9d00c-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-203">Motor</span><span class="sxs-lookup"><span data-stu-id="9d00c-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="9d00c-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-205">Texto</span><span class="sxs-lookup"><span data-stu-id="9d00c-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="9d00c-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="9d00c-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-208">Archivos HTML (*.ht*)</span><span class="sxs-lookup"><span data-stu-id="9d00c-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="9d00c-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="9d00c-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-211">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="9d00c-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="9d00c-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-214">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="9d00c-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="9d00c-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9d00c-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="9d00c-217">2 </span><span class="sxs-lookup"><span data-stu-id="9d00c-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="9d00c-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="9d00c-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-220">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="9d00c-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-223">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="9d00c-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p117">Importar datos del archivo externo a la base de datos activa. Al cambiar datos en la base de datos activa, no cambiarán los del archivo externo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p117">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="9d00c-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="9d00c-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p118">Crear una tabla en la base de datos activa que está vinculada al archivo externo. Si se cambian datos en la base de datos activa, también cambiarán los del archivo externo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p118">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="9d00c-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="9d00c-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-234">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9d00c-235">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="9d00c-236">Formatos ISAM de exportación HTML</span><span class="sxs-lookup"><span data-stu-id="9d00c-236">HTML export ISAM formats</span></span>

<span data-ttu-id="9d00c-237">La **carpeta Exportación HTML de \\ \\ formatos HTML** del motor de conectividad de Access contiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="9d00c-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d00c-238">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="9d00c-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="9d00c-239">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d00c-239">Type</span></span></p></th>
<th><p><span data-ttu-id="9d00c-240">Valor</span><span class="sxs-lookup"><span data-stu-id="9d00c-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-241">Motor</span><span class="sxs-lookup"><span data-stu-id="9d00c-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="9d00c-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-243">Texto</span><span class="sxs-lookup"><span data-stu-id="9d00c-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="9d00c-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="9d00c-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-246">Archivos HTML (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="9d00c-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="9d00c-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="9d00c-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-249">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="9d00c-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="9d00c-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-252">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="9d00c-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="9d00c-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9d00c-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="9d00c-255">2 </span><span class="sxs-lookup"><span data-stu-id="9d00c-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="9d00c-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="9d00c-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-258">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="9d00c-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-261">00</span><span class="sxs-lookup"><span data-stu-id="9d00c-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="9d00c-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="9d00c-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9d00c-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p119">Exportar datos de la base de datos activa a un archivo de texto. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p119">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="9d00c-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="9d00c-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9d00c-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9d00c-268">01</span><span class="sxs-lookup"><span data-stu-id="9d00c-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9d00c-269">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="9d00c-270">Personalización del archivo Schema.ini para texto y datos HTML</span><span class="sxs-lookup"><span data-stu-id="9d00c-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="9d00c-p120">Para poder leer, importar o exportar texto y datos HTML, es necesario crear un archivo Schema.ini e incluir la información ISAM de texto en dicho archivo. El archivo Schema.ini contiene información detallada sobre un origen de datos: cómo se da formato al archivo de texto, cómo se lee en el momento de la importación y cuál es el formato de exportación predeterminado para los archivos. Los ejemplos siguientes muestran el diseño para un archivo de ancho fijo, Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="9d00c-p120">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

<span data-ttu-id="9d00c-274">De forma similar, el formato para un archivo delimitado se especifica de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d00c-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

<span data-ttu-id="9d00c-275">Si está exportando datos a un archivo de texto delimitado, especifique también el formato de dicho archivo:</span><span class="sxs-lookup"><span data-stu-id="9d00c-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

<span data-ttu-id="9d00c-p121">El ejemplo My Special Export hace referencia a una opción de exportación determinada; es posible especificar cualquier variación de las opciones de exportación a la hora de realizar la conexión. Este último ejemplo también corresponde a un nombre de origen de datos (DSN) que se puede pasar de forma opcional al efectuar la conexión. Se pueden incluir las tres secciones de formato en el mismo archivo .ini.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p121">The My Special Export example refers to a specific export option; you can specify any variation of export options at connect time. This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time. All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="9d00c-279">El motor de base de datos de Microsoft Access utiliza las entradas del archivo Schema.ini de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="9d00c-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d00c-280">Entrada</span><span class="sxs-lookup"><span data-stu-id="9d00c-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="9d00c-281">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d00c-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="9d00c-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="9d00c-283">Se puede establecer en <strong>True</strong> (que indica que el primer registro de datos especifica los nombres de las columnas) o en <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d00c-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-284">Formato</span><span class="sxs-lookup"><span data-stu-id="9d00c-284">Format</span></span></p></td>
<td><p><span data-ttu-id="9d00c-285">Puede establecerse en uno de los siguientes valores: TabDelimited, CSVDelimited, Delimited ( &lt; single character ) o &gt; FixedLength.</span><span class="sxs-lookup"><span data-stu-id="9d00c-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="9d00c-286">El delimitador especificado para el formato de archivo Delimitado puede ser cualquier carácter único excepto una comilla doble ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="9d00c-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="9d00c-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="9d00c-288">Sólo se utiliza cuando el formato es FixedLength y se puede establecer en uno de los valores siguientes: RaggedEdge o TrueFixedLength.</span><span class="sxs-lookup"><span data-stu-id="9d00c-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="9d00c-289">RaggedEdge permite terminar las filas con un carácter de retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="9d00c-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="9d00c-290">TrueFixedLength requiere que cada fila tenga un número exacto de caracteres, y se supone que todos los caracteres de retorno de carro que no están en el límite de la fila están incrustado en un campo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="9d00c-291">Si este valor no está presente, el valor predeterminado es RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="9d00c-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="9d00c-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p124">Indica el número de filas que se van a examinar para estimar los tipos de datos de las columnas. Si se establece en 0, se analizará el archivo completo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p124">Indicates the number of rows to be scanned when guessing the column data types. If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="9d00c-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="9d00c-296">Se pueden establecer en OEM, ANSI, UNICODE o en el número decimal de una página de códigos válida, e indica el juego de caracteres del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="9d00c-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9d00c-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p125">Puede establecerse en una cadena de formato que indica fechas y horas. Esta entrada debe especificarse si durante la importación/exportación todos los campos de fecha y hora se manejan con el mismo formato. Se admiten todos los formatos del motor de base de datos Microsoft Jet, excepto a.m. y p.m. En ausencia de una cadena de formato, se utilizarán las opciones de fecha y hora cortas del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p125">Can be set to a format string indicating dates and times. This entry should be specified if all date/time fields in the import/export are handled with the same format. All of the Microsoft Jet database engine formats except AM and PM are supported. In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="9d00c-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p126">Indica el símbolo de moneda que se va a utilizar para los valores monetarios en el archivo de texto. Por ejemplo, el signo de dólar ($) y el marco alemán. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p126">Indicates the currency symbol to be used for currency values in the text file. Examples include the dollar sign ($) and Dm. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="9d00c-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="9d00c-307">Se puede establecer en cualquiera de los siguientes valores: Prefijo de símbolo de moneda sin separación ($1) Sufijo de símbolo de moneda sin separación (1$) Prefijo de símbolo de moneda con una separación de caracteres ($ 1) Sufijo de símbolo de moneda con una separación de caracteres (1 $) Si esta entrada no está presente, se usa el valor predeterminado en el Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="9d00c-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p127">Especifica el número de dígitos utilizado para la parte fraccionaria de una cantidad de moneda. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p127">Specifies the number of digits used for the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="9d00c-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="9d00c-312">Puede ser uno de los siguientes valores: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) El signo de dólar se muestra para este ejemplo, pero debe reemplazarse por el valor CurrencySymbol apropiado en el programa real.</span><span class="sxs-lookup"><span data-stu-id="9d00c-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="9d00c-313">Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="9d00c-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p129">Indica el símbolo de carácter único que se va a utilizar como separador de miles para los valores monetarios en el archivo de texto. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p129">Indicates the single-character symbol to be used for separating currency values by thousands in the text file. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="9d00c-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p130">Puede establecerse en cualquier carácter único que se utilice para separar la parte entera de la parte fraccionaria de una cantidad de moneda. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p130">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="9d00c-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p131">Puede establecerse en cualquier carácter único que se utilice para separar la parte entera de la fraccionaria de un número. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p131">Can be set to any single character that is used to separate the integer from the fractional part of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="9d00c-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="9d00c-p132">Indica el número de dígitos decimales de la parte fraccionaria de un número. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="9d00c-p132">Indicates the number of decimal digits in the fractional portion of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="9d00c-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="9d00c-327">Especifica si un valor decimal menor que 1 y mayor que –1 debe incluir ceros no significativos; este valor puede ser False (no incluir ceros no significativos) o True.</span><span class="sxs-lookup"><span data-stu-id="9d00c-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d00c-328">Col1, Col2, ...</span><span class="sxs-lookup"><span data-stu-id="9d00c-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="9d00c-329">Indica las columnas del archivo de texto que se deben leer.</span><span class="sxs-lookup"><span data-stu-id="9d00c-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="9d00c-330">El formato de esta entrada debe ser: <em>Coln</em> = <em>columnName</em> type [Width <em>#</em> ] <em>columnName</em>: Column names with embedded spaces should be entre comillas.</span><span class="sxs-lookup"><span data-stu-id="9d00c-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="9d00c-331"><em>tipo</em>: Puede ser Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="9d00c-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="9d00c-332">Binary, OLE, Text o Memo.</span><span class="sxs-lookup"><span data-stu-id="9d00c-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="9d00c-333">Además, se admiten los siguientes tipos de controladores de texto ODBC: El formato de fecha Char (igual que Text) Float (igual que Double) Integer (igual que Short) LongChar (igual que Memo) Formato de fecha <em>En</em> el caso de un tipo memo, se puede usar un marcador de formato adicional [Hipervínculo de atributo] para especificar columnas que deben ser direcciones URL activas en Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9d00c-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="9d00c-334">En el caso del tipo Decimal, deben utilizarse los marcadores de formato adicionales [Scale #] Precision #].</span><span class="sxs-lookup"><span data-stu-id="9d00c-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d00c-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="9d00c-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="9d00c-336">Puede establecerse en cualquier carácter único que se utilice para delimitar cadenas que contengan cualquiera de los demás caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="9d00c-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="9d00c-337">Por ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d00c-337">E.g.</span></span> <span data-ttu-id="9d00c-338">&quot;abc &quot; , &quot; xyz,pqr , hij Si esta entrada no está presente, el delimitador predeterminado &quot; es una comilla &quot; &quot; doble.</span><span class="sxs-lookup"><span data-stu-id="9d00c-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="9d00c-339">Si esta entrada es la cadena none, no se tratarán caracteres &quot; &quot; como delimitadores.</span><span class="sxs-lookup"><span data-stu-id="9d00c-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9d00c-340">[!NOTA] Si modifica la configuración del archivo Schema.ini, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="9d00c-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


