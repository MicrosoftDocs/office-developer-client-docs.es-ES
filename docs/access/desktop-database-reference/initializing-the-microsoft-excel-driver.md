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
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="3f1f2-102">Inicialización del controlador de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="3f1f2-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="3f1f2-103">**Se aplica a**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office para empresas Access 2013 | Excel 2010 | Access 2010</span><span class="sxs-lookup"><span data-stu-id="3f1f2-103">**Applies to**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for business Access 2013 | Excel 2010 | Access 2010</span></span>

<span data-ttu-id="3f1f2-104">Al instalar el controlador de Excel, el programa de instalación escribe un conjunto de valores predeterminados en el Registro de Windows en las subclaves Engines e ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="3f1f2-105">No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="3f1f2-106">Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="3f1f2-107">Configuración de inicialización de Excel</span><span class="sxs-lookup"><span data-stu-id="3f1f2-107">Excel initialization settings</span></span>

<span data-ttu-id="3f1f2-108">La carpeta De Excel de los motores de conectividad de **Access \\ \\** incluye la configuración de inicialización del controlador Aceexcl.dll, que se usa para el acceso externo a las hojas de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="3f1f2-109">En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="3f1f2-110">El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Excel de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f1f2-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f1f2-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="3f1f2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f1f2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-113">win32</span><span class="sxs-lookup"><span data-stu-id="3f1f2-113">win32</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-p103">Ubicación de msexcl40.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f1f2-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="3f1f2-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-118">Número de filas en las que se va a comprobar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="3f1f2-119">Éste se determina de acuerdo al número máximo de clases de datos que se encuentren.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="3f1f2-120">Si no es posible hacerlo de esta manera, se determinará en el siguiente orden: Número, Moneda, Fecha, Texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="3f1f2-121">Si se encuentran datos que no coinciden con el tipo de datos estimado para la columna, se devuelven como un valor <strong>Null</strong>.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="3f1f2-122">A la hora de realizar la importación, si una columna tiene tipos de datos mixtos, toda la columna se convertirá de acuerdo con el valor de ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="3f1f2-123">El número predeterminado de filas que se van a comprobar es 8.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="3f1f2-124">Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="3f1f2-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-p105">Su valor se puede establecer en MajorityType o Text. Si se establece en MajorityType, las columnas con tipos de datos mixtos se convertirán al tipo de datos predominante en la importación. Si se establece como Text, las columnas con tipos de datos mixtos se convertirán a texto en la importación. El valor predeterminado es Text. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f1f2-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="3f1f2-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-p106">Número de filas en blanco que se deben agregar al final de una hoja de cálculo de la Versión 3.5 o 4.0 antes de que se agreguen nuevos datos. Por ejemplo, si se establece AppendBlankRows en 4, Microsoft Jet agregará 4 filas en blanco al final de la hoja de cálculo antes de agregar filas que contengan datos. Los valores enteros para esta configuración pueden oscilar entre 0 y 16; el valor predeterminado es 01 (se agrega una fila adicional). Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="3f1f2-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-p107">Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila. Un valor de 00 indica que no hay nombres de columna en la primera fila; dichos nombres aparecerán como F1, F2, F3, etc. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="3f1f2-142">La carpeta Motores de conectividad de **\\ Access Excel \\ 8.0** contiene las siguientes entradas, que se aplican a Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f1f2-143">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="3f1f2-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="3f1f2-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f1f2-144">Type</span></span></p></th>
<th><p><span data-ttu-id="3f1f2-145">Valor</span><span class="sxs-lookup"><span data-stu-id="3f1f2-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-146">Motor</span><span class="sxs-lookup"><span data-stu-id="3f1f2-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="3f1f2-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-148">Excel</span><span class="sxs-lookup"><span data-stu-id="3f1f2-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f1f2-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="3f1f2-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="3f1f2-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="3f1f2-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="3f1f2-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f1f2-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-154">01</span><span class="sxs-lookup"><span data-stu-id="3f1f2-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f1f2-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="3f1f2-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f1f2-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-157">00</span><span class="sxs-lookup"><span data-stu-id="3f1f2-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="3f1f2-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="3f1f2-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-160">1 </span><span class="sxs-lookup"><span data-stu-id="3f1f2-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f1f2-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="3f1f2-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f1f2-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-163">00</span><span class="sxs-lookup"><span data-stu-id="3f1f2-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="3f1f2-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f1f2-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-166">01</span><span class="sxs-lookup"><span data-stu-id="3f1f2-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f1f2-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="3f1f2-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="3f1f2-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-p108">Exportar datos de la base de datos activa a un archivo de Microsoft Excel 97. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f1f2-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="3f1f2-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f1f2-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="3f1f2-173">01</span><span class="sxs-lookup"><span data-stu-id="3f1f2-173">01</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="3f1f2-174">Uso de la configuración TypeGuessRows para el controlador de Excel</span><span class="sxs-lookup"><span data-stu-id="3f1f2-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="3f1f2-175">Al usar el controlador de Microsoft Excel, puede usar el valor del Registro **TypeGuessRows** para configurar cuántas filas se van a comprobar para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="3f1f2-176">El **valor TypeGuessRows** se encuentra en la siguiente subclave del Registro:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016"></a>[<span data-ttu-id="3f1f2-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="3f1f2-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="3f1f2-178">Para una instalación MSI de Office</span><span class="sxs-lookup"><span data-stu-id="3f1f2-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="3f1f2-179">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="3f1f2-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="3f1f2-181">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="3f1f2-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="3f1f2-183">Para una instalación de Hacer clic y ejecutar de Office</span><span class="sxs-lookup"><span data-stu-id="3f1f2-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="3f1f2-184">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="3f1f2-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="3f1f2-186">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="3f1f2-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="3f1f2-188">El número predeterminado de filas que se deben comprobar es **8** (ocho).</span><span class="sxs-lookup"><span data-stu-id="3f1f2-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="3f1f2-189">Cuando se establece el valor **typeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="3f1f2-190">Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el rango deseado.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="3f1f2-191">Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitido en Excel).</span><span class="sxs-lookup"><span data-stu-id="3f1f2-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="3f1f2-192">El tipo de datos está determinado por el número máximo de tipos de datos que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="3f1f2-193">Si hay un empate, el tipo de datos se determina en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="3f1f2-194">Número</span><span class="sxs-lookup"><span data-stu-id="3f1f2-194">Number</span></span>
- <span data-ttu-id="3f1f2-195">Divisa</span><span class="sxs-lookup"><span data-stu-id="3f1f2-195">Currency</span></span>
- <span data-ttu-id="3f1f2-196">Fecha</span><span class="sxs-lookup"><span data-stu-id="3f1f2-196">Date</span></span>
- <span data-ttu-id="3f1f2-197">Texto</span><span class="sxs-lookup"><span data-stu-id="3f1f2-197">Text</span></span>
- <span data-ttu-id="3f1f2-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="3f1f2-198">Boolean</span></span>

<span data-ttu-id="3f1f2-199">Si se encuentran datos que no coinciden con el tipo de datos calculado para la columna, estos datos se devuelven como **un valor** Null.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="3f1f2-200">Durante una importación, si una columna tiene tipos de datos mixtos, toda la columna se convierte en el tipo de datos establecido por la configuración **ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013"></a>[<span data-ttu-id="3f1f2-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f1f2-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="3f1f2-202">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="3f1f2-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="3f1f2-204">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="3f1f2-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="3f1f2-206">El número predeterminado de filas que se deben comprobar es **8** (ocho).</span><span class="sxs-lookup"><span data-stu-id="3f1f2-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="3f1f2-207">Cuando se establece el valor **typeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="3f1f2-208">Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el rango deseado.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="3f1f2-209">Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitido en Excel).</span><span class="sxs-lookup"><span data-stu-id="3f1f2-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="3f1f2-210">El tipo de datos está determinado por el número máximo de tipos de datos que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="3f1f2-211">Si hay un empate, el tipo de datos se determina en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="3f1f2-212">Número</span><span class="sxs-lookup"><span data-stu-id="3f1f2-212">Number</span></span>
- <span data-ttu-id="3f1f2-213">Divisa</span><span class="sxs-lookup"><span data-stu-id="3f1f2-213">Currency</span></span>
- <span data-ttu-id="3f1f2-214">Fecha</span><span class="sxs-lookup"><span data-stu-id="3f1f2-214">Date</span></span>
- <span data-ttu-id="3f1f2-215">Texto</span><span class="sxs-lookup"><span data-stu-id="3f1f2-215">Text</span></span>
- <span data-ttu-id="3f1f2-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="3f1f2-216">Boolean</span></span>

<span data-ttu-id="3f1f2-217">Si se encuentran datos que no coinciden con el tipo de datos calculado para la columna, estos datos se devuelven como **un valor** Null.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="3f1f2-218">Durante una importación, si una columna tiene tipos de datos mixtos, toda la columna se convierte en el tipo de datos establecido por la configuración **ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010"></a>[<span data-ttu-id="3f1f2-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="3f1f2-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="3f1f2-220">Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="3f1f2-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="3f1f2-222">Para Office de 32 bits en Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="3f1f2-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="3f1f2-224">El número predeterminado de filas que se deben comprobar es **8** (ocho).</span><span class="sxs-lookup"><span data-stu-id="3f1f2-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="3f1f2-225">Cuando se establece el valor **typeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="3f1f2-226">Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el rango deseado.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="3f1f2-227">Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitido en Excel).</span><span class="sxs-lookup"><span data-stu-id="3f1f2-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="3f1f2-228">El tipo de datos está determinado por el número máximo de tipos de datos que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="3f1f2-229">Si hay un empate, el tipo de datos se determina en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="3f1f2-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="3f1f2-230">Número</span><span class="sxs-lookup"><span data-stu-id="3f1f2-230">Number</span></span>
- <span data-ttu-id="3f1f2-231">Divisa</span><span class="sxs-lookup"><span data-stu-id="3f1f2-231">Currency</span></span>
- <span data-ttu-id="3f1f2-232">Fecha</span><span class="sxs-lookup"><span data-stu-id="3f1f2-232">Date</span></span>
- <span data-ttu-id="3f1f2-233">Texto</span><span class="sxs-lookup"><span data-stu-id="3f1f2-233">Text</span></span>
- <span data-ttu-id="3f1f2-234">Booleano</span><span class="sxs-lookup"><span data-stu-id="3f1f2-234">Boolean</span></span>

<span data-ttu-id="3f1f2-235">Si se encuentran datos que no coinciden con el tipo de datos calculado para la columna, estos datos se devuelven como **un valor** Null.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="3f1f2-236">Durante una importación, si una columna tiene tipos de datos mixtos, toda la columna se convierte en el tipo de datos establecido por la configuración **ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="3f1f2-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="3f1f2-237">[!NOTA] Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="3f1f2-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f1f2-238">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3f1f2-238">See also</span></span>

- [<span data-ttu-id="3f1f2-239">Uso de la configuración TypeGuessRows para el controlador de Excel</span><span class="sxs-lookup"><span data-stu-id="3f1f2-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

