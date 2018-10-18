---
title: Inicializar el controlador de Microsoft Excel
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7c9a3282f3bb508a4c68ecbd3f2c0465cfee9bac
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603101"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="bab24-102">Inicializar el controlador de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="bab24-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="bab24-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bab24-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bab24-104"><<<<<<< HEAD al instalar el controlador de Microsoft® Excel, el programa de instalación escribe un conjunto de valores predeterminados en el registro de Microsoft Windows®, en las subclaves de los motores y los formatos ISAM.</span><span class="sxs-lookup"><span data-stu-id="bab24-104"><<<<<<< HEAD When you install the Microsoft® Excel driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="bab24-105">No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bab24-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="bab24-106">Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bab24-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="microsoft-excel-initialization-settings"></a><span data-ttu-id="bab24-107">Configuración de inicialización de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="bab24-107">Microsoft Excel Initialization Settings</span></span>
<span data-ttu-id="bab24-108">=== Al instalar el controlador de Excel, el programa de instalación escribe un conjunto de valores predeterminados en el registro de Windows en las subclaves de los motores y los formatos ISAM.</span><span class="sxs-lookup"><span data-stu-id="bab24-108">======= When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="bab24-109">No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bab24-109">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="bab24-110">Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bab24-110">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="bab24-111">Configuración de inicialización de Excel</span><span class="sxs-lookup"><span data-stu-id="bab24-111">Excel Initialization Settings</span></span>
>>>>>>> <span data-ttu-id="bab24-112">master</span><span class="sxs-lookup"><span data-stu-id="bab24-112">master</span></span>

<span data-ttu-id="bab24-113">La **Access Connectivity Engine\\motores\\Excel** carpeta incluye la configuración de inicialización para el controlador Aceexcl.dll, utilizado para el acceso externo a hojas de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bab24-113">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="bab24-114">En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="bab24-114">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="bab24-115">El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Excel de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="bab24-115">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bab24-116">Entrada</span><span class="sxs-lookup"><span data-stu-id="bab24-116">Entry</span></span></p></th>
<th><p><span data-ttu-id="bab24-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bab24-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab24-118">Win32</span><span class="sxs-lookup"><span data-stu-id="bab24-118">win32</span></span></p></td>
<td><p><span data-ttu-id="bab24-p104">Ubicación de msexcl40.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bab24-p104">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab24-122">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="bab24-122">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="bab24-123">El número de filas que se puede comprobar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bab24-123">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="bab24-124">Se determina el tipo de datos dado el número máximo de tipos de datos que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="bab24-124">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="bab24-125">Si no hay una placa, se determina el tipo de datos en el siguiente orden: número, moneda, fecha, texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="bab24-125">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="bab24-126">Si se encuentran datos que no coincide con el tipo de datos estimado para la columna, se devuelve como un valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="bab24-126">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="bab24-127">En la importación, si una columna tiene distintos tipos de datos, se convertirá la columna entera según la configuración de ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="bab24-127">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="bab24-128">El número predeterminado de filas que se va a comprobar es 8.</span><span class="sxs-lookup"><span data-stu-id="bab24-128">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="bab24-129">Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="bab24-129">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab24-130">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="bab24-130">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="bab24-p106">Su valor se puede establecer en MajorityType o Text. Si se establece en MajorityType, las columnas con tipos de datos mixtos se convertirán al tipo de datos predominante en la importación. Si se establece como Text, las columnas con tipos de datos mixtos se convertirán a texto en la importación. El valor predeterminado es Text. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bab24-p106">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab24-136">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="bab24-136">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="bab24-p107">Número de filas en blanco que se deben agregar al final de una hoja de cálculo de la Versión 3.5 o 4.0 antes de que se agreguen nuevos datos. Por ejemplo, si se establece AppendBlankRows en 4, Microsoft Jet agregará 4 filas en blanco al final de la hoja de cálculo antes de agregar filas que contengan datos. Los valores enteros para esta configuración pueden oscilar entre 0 y 16; el valor predeterminado es 01 (se agrega una fila adicional). Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="bab24-p107">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab24-141">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="bab24-141">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="bab24-p108">Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila. Un valor de 00 indica que no hay nombres de columna en la primera fila; dichos nombres aparecerán como F1, F2, F3, etc. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="bab24-p108">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab24-147">La **Access Connectivity Engine\\motores\\Excel 8.0** carpeta contiene las siguientes entradas, que se aplican a Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="bab24-147">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bab24-148">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="bab24-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bab24-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="bab24-149">Type</span></span></p></th>
<th><p><span data-ttu-id="bab24-150">Valor</span><span class="sxs-lookup"><span data-stu-id="bab24-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab24-151">Engine</span><span class="sxs-lookup"><span data-stu-id="bab24-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="bab24-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bab24-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bab24-153">Excel</span><span class="sxs-lookup"><span data-stu-id="bab24-153">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab24-154">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="bab24-154">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="bab24-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bab24-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bab24-156">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="bab24-156">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab24-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="bab24-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bab24-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bab24-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bab24-159">01</span><span class="sxs-lookup"><span data-stu-id="bab24-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab24-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="bab24-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bab24-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bab24-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bab24-162">00</span><span class="sxs-lookup"><span data-stu-id="bab24-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab24-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="bab24-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bab24-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bab24-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bab24-165">1</span><span class="sxs-lookup"><span data-stu-id="bab24-165">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab24-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="bab24-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bab24-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bab24-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bab24-168">00</span><span class="sxs-lookup"><span data-stu-id="bab24-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab24-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="bab24-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bab24-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bab24-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bab24-171">01</span><span class="sxs-lookup"><span data-stu-id="bab24-171">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab24-172">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="bab24-172">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="bab24-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bab24-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bab24-p109">Exportar datos de la base de datos activa a un archivo de Microsoft Excel 97. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="bab24-p109">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab24-176">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="bab24-176">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bab24-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bab24-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bab24-178">01</span><span class="sxs-lookup"><span data-stu-id="bab24-178">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="bab24-179">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="bab24-179">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

<span data-ttu-id="bab24-180"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="bab24-180"><<<<<<< HEAD</span></span>

=======
## <a name="see-also"></a><span data-ttu-id="bab24-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="bab24-181">See also</span></span>

[<span data-ttu-id="bab24-182">Utilizando la configuración de TypeGuessRows para el controlador de Excel</span><span class="sxs-lookup"><span data-stu-id="bab24-182">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
>>>>>>> <span data-ttu-id="bab24-183">master</span><span class="sxs-lookup"><span data-stu-id="bab24-183">master</span></span>
