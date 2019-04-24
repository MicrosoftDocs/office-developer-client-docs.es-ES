---
title: Inicialización del controlador de Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291438"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="5aea5-102">Inicialización del controlador de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="5aea5-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="5aea5-103">**Se aplica a**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office para empresas Access 2013 | Excel 2010 | Access 2010</span><span class="sxs-lookup"><span data-stu-id="5aea5-103">**Applies to**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for business Access 2013 | Excel 2010 | Access 2010</span></span>

<span data-ttu-id="5aea5-104">Cuando se instala el controlador de Excel, el programa de instalación escribe un conjunto de valores predeterminados en el registro de Windows, en las subclaves de los motores y los formatos ISAM.</span><span class="sxs-lookup"><span data-stu-id="5aea5-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="5aea5-105">No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5aea5-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="5aea5-106">Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5aea5-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="5aea5-107">Configuración de inicialización de Excel</span><span class="sxs-lookup"><span data-stu-id="5aea5-107">Excel initialization settings</span></span>

<span data-ttu-id="5aea5-108">La carpeta de **Excel\\motores\\del motor de conectividad de Access** incluye la configuración de inicialización del controlador Aceexcl. dll, que se usa para el acceso externo a las hojas de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="5aea5-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="5aea5-109">En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="5aea5-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="5aea5-110">El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Excel de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="5aea5-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5aea5-111">Inserción</span><span class="sxs-lookup"><span data-stu-id="5aea5-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="5aea5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aea5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-113">Win32</span><span class="sxs-lookup"><span data-stu-id="5aea5-113">win32</span></span></p></td>
<td><p><span data-ttu-id="5aea5-p103">Ubicación de msexcl40.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="5aea5-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aea5-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="5aea5-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="5aea5-118">Número de filas en las que se va a comprobar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5aea5-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="5aea5-119">Éste se determina de acuerdo al número máximo de clases de datos que se encuentren.</span><span class="sxs-lookup"><span data-stu-id="5aea5-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="5aea5-120">Si no es posible hacerlo de esta manera, se determinará en el siguiente orden: Número, Moneda, Fecha, Texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="5aea5-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="5aea5-121">Si se encuentran datos que no coinciden con el tipo de datos estimado para la columna, se devuelven como un valor <strong>Null</strong>.</span><span class="sxs-lookup"><span data-stu-id="5aea5-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="5aea5-122">A la hora de realizar la importación, si una columna tiene tipos de datos mixtos, toda la columna se convertirá de acuerdo con el valor de ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="5aea5-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="5aea5-123">El número predeterminado de filas que se van a comprobar es 8.</span><span class="sxs-lookup"><span data-stu-id="5aea5-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="5aea5-124">Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="5aea5-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="5aea5-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="5aea5-p105">Su valor se puede establecer en MajorityType o Text. Si se establece en MajorityType, las columnas con tipos de datos mixtos se convertirán al tipo de datos predominante en la importación. Si se establece como Text, las columnas con tipos de datos mixtos se convertirán a texto en la importación. El valor predeterminado es Text. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="5aea5-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aea5-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="5aea5-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="5aea5-p106">Número de filas en blanco que se deben agregar al final de una hoja de cálculo de la Versión 3.5 o 4.0 antes de que se agreguen nuevos datos. Por ejemplo, si se establece AppendBlankRows en 4, Microsoft Jet agregará 4 filas en blanco al final de la hoja de cálculo antes de agregar filas que contengan datos. Los valores enteros para esta configuración pueden oscilar entre 0 y 16; el valor predeterminado es 01 (se agrega una fila adicional). Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="5aea5-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="5aea5-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="5aea5-p107">Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila. Un valor de 00 indica que no hay nombres de columna en la primera fila; dichos nombres aparecerán como F1, F2, F3, etc. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="5aea5-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="5aea5-142">La carpeta **Excel 8,0\\de\\los motores del motor de conectividad de Access** contiene las siguientes entradas, que se aplican a Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="5aea5-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5aea5-143">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="5aea5-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="5aea5-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="5aea5-144">Type</span></span></p></th>
<th><p><span data-ttu-id="5aea5-145">Valor</span><span class="sxs-lookup"><span data-stu-id="5aea5-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-146">Prototipo</span><span class="sxs-lookup"><span data-stu-id="5aea5-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="5aea5-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5aea5-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5aea5-148">Excel</span><span class="sxs-lookup"><span data-stu-id="5aea5-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aea5-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="5aea5-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="5aea5-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5aea5-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5aea5-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="5aea5-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="5aea5-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="5aea5-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5aea5-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5aea5-154">00</span><span class="sxs-lookup"><span data-stu-id="5aea5-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aea5-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="5aea5-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="5aea5-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5aea5-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5aea5-157">4,00</span><span class="sxs-lookup"><span data-stu-id="5aea5-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="5aea5-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="5aea5-159">DWORD</span><span class="sxs-lookup"><span data-stu-id="5aea5-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="5aea5-160">1</span><span class="sxs-lookup"><span data-stu-id="5aea5-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aea5-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="5aea5-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="5aea5-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5aea5-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5aea5-163">4,00</span><span class="sxs-lookup"><span data-stu-id="5aea5-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="5aea5-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="5aea5-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5aea5-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5aea5-166">00</span><span class="sxs-lookup"><span data-stu-id="5aea5-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aea5-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="5aea5-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="5aea5-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5aea5-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="5aea5-p108">Exportar datos de la base de datos activa a un archivo de Microsoft Excel 97. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="5aea5-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aea5-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="5aea5-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="5aea5-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="5aea5-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="5aea5-173">00</span><span class="sxs-lookup"><span data-stu-id="5aea5-173">01</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="5aea5-174">Uso de la configuración TypeGuessRows para el controlador de Excel</span><span class="sxs-lookup"><span data-stu-id="5aea5-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="5aea5-175">Cuando se usa un controlador de Microsoft Excel, se puede usar el valor del registro **TypeGuessRows** para configurar el número de filas que se van a comprobar para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5aea5-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="5aea5-176">El valor **TypeGuessRows** se encuentra en la siguiente subclave del registro:</span><span class="sxs-lookup"><span data-stu-id="5aea5-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016taboffice-2016"></a>[<span data-ttu-id="5aea5-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="5aea5-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="5aea5-178">Para una instalación MSI de Office</span><span class="sxs-lookup"><span data-stu-id="5aea5-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="5aea5-179">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="5aea5-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="5aea5-181">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="5aea5-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="5aea5-183">Para una instalación de hacer clic y ejecutar de Office</span><span class="sxs-lookup"><span data-stu-id="5aea5-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="5aea5-184">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="5aea5-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="5aea5-186">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="5aea5-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="5aea5-188">El número predeterminado de filas que se va a comprobar es **8** (ocho).</span><span class="sxs-lookup"><span data-stu-id="5aea5-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="5aea5-189">Cuando se establece el valor **TypeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5aea5-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="5aea5-190">Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado.</span><span class="sxs-lookup"><span data-stu-id="5aea5-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="5aea5-191">Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitidas en Excel).</span><span class="sxs-lookup"><span data-stu-id="5aea5-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="5aea5-192">El tipo de datos se determina por el número máximo de tipos de datos que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="5aea5-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="5aea5-193">Si hay una empate, el tipo de datos se determina en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="5aea5-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="5aea5-194">Número</span><span class="sxs-lookup"><span data-stu-id="5aea5-194">Number</span></span>
- <span data-ttu-id="5aea5-195">Moneda</span><span class="sxs-lookup"><span data-stu-id="5aea5-195">Currency</span></span>
- <span data-ttu-id="5aea5-196">Fecha</span><span class="sxs-lookup"><span data-stu-id="5aea5-196">Date</span></span>
- <span data-ttu-id="5aea5-197">Texto</span><span class="sxs-lookup"><span data-stu-id="5aea5-197">Text</span></span>
- <span data-ttu-id="5aea5-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="5aea5-198">Boolean</span></span>

<span data-ttu-id="5aea5-199">Si se encuentran datos que no coinciden con el tipo de datos adivinados para la columna, esos datos se devuelven como un valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5aea5-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="5aea5-200">Durante una importación, si una columna tiene tipos de datos mezclados, toda la columna se convierte en el tipo de datos que establece la configuración **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="5aea5-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013taboffice-2013"></a>[<span data-ttu-id="5aea5-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="5aea5-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="5aea5-202">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="5aea5-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="5aea5-204">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="5aea5-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="5aea5-206">El número predeterminado de filas que se va a comprobar es **8** (ocho).</span><span class="sxs-lookup"><span data-stu-id="5aea5-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="5aea5-207">Cuando se establece el valor **TypeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5aea5-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="5aea5-208">Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado.</span><span class="sxs-lookup"><span data-stu-id="5aea5-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="5aea5-209">Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitidas en Excel).</span><span class="sxs-lookup"><span data-stu-id="5aea5-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="5aea5-210">El tipo de datos se determina por el número máximo de tipos de datos que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="5aea5-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="5aea5-211">Si hay una empate, el tipo de datos se determina en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="5aea5-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="5aea5-212">Número</span><span class="sxs-lookup"><span data-stu-id="5aea5-212">Number</span></span>
- <span data-ttu-id="5aea5-213">Moneda</span><span class="sxs-lookup"><span data-stu-id="5aea5-213">Currency</span></span>
- <span data-ttu-id="5aea5-214">Fecha</span><span class="sxs-lookup"><span data-stu-id="5aea5-214">Date</span></span>
- <span data-ttu-id="5aea5-215">Texto</span><span class="sxs-lookup"><span data-stu-id="5aea5-215">Text</span></span>
- <span data-ttu-id="5aea5-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="5aea5-216">Boolean</span></span>

<span data-ttu-id="5aea5-217">Si se encuentran datos que no coinciden con el tipo de datos adivinados para la columna, esos datos se devuelven como un valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5aea5-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="5aea5-218">Durante una importación, si una columna tiene tipos de datos mezclados, toda la columna se convierte en el tipo de datos que establece la configuración **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="5aea5-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010taboffice-2010"></a>[<span data-ttu-id="5aea5-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="5aea5-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="5aea5-220">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="5aea5-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="5aea5-222">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5aea5-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="5aea5-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="5aea5-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="5aea5-224">El número predeterminado de filas que se va a comprobar es **8** (ocho).</span><span class="sxs-lookup"><span data-stu-id="5aea5-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="5aea5-225">Cuando se establece el valor **TypeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5aea5-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="5aea5-226">Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado.</span><span class="sxs-lookup"><span data-stu-id="5aea5-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="5aea5-227">Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitidas en Excel).</span><span class="sxs-lookup"><span data-stu-id="5aea5-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="5aea5-228">El tipo de datos se determina por el número máximo de tipos de datos que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="5aea5-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="5aea5-229">Si hay una empate, el tipo de datos se determina en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="5aea5-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="5aea5-230">Número</span><span class="sxs-lookup"><span data-stu-id="5aea5-230">Number</span></span>
- <span data-ttu-id="5aea5-231">Moneda</span><span class="sxs-lookup"><span data-stu-id="5aea5-231">Currency</span></span>
- <span data-ttu-id="5aea5-232">Fecha</span><span class="sxs-lookup"><span data-stu-id="5aea5-232">Date</span></span>
- <span data-ttu-id="5aea5-233">Texto</span><span class="sxs-lookup"><span data-stu-id="5aea5-233">Text</span></span>
- <span data-ttu-id="5aea5-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="5aea5-234">Boolean</span></span>

<span data-ttu-id="5aea5-235">Si se encuentran datos que no coinciden con el tipo de datos adivinados para la columna, esos datos se devuelven como un valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5aea5-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="5aea5-236">Durante una importación, si una columna tiene tipos de datos mezclados, toda la columna se convierte en el tipo de datos que establece la configuración **ImportMixedTypes** .</span><span class="sxs-lookup"><span data-stu-id="5aea5-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="5aea5-237">[!NOTA] Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="5aea5-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="5aea5-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aea5-238">See also</span></span>

- [<span data-ttu-id="5aea5-239">Uso de la configuración TypeGuessRows para el controlador de Excel</span><span class="sxs-lookup"><span data-stu-id="5aea5-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

