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
ms.openlocfilehash: c79d859b122eb3595c31b2ffcec192e2d69ed7b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486402"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="1c588-102">Inicializar el controlador de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="1c588-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="1c588-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c588-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1c588-p101">Cuando se instala el controlador de Microsoft® Excel, el programa de instalación escribe un conjunto de valores predeterminados en el Registro de Microsoft Windows®, concretamente en las subclaves Engines e ISAM Formats. No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación. Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1c588-p101">When you install the Microsoft® Excel driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="microsoft-excel-initialization-settings"></a><span data-ttu-id="1c588-107">Configuración de inicialización de Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="1c588-107">Microsoft Excel Initialization Settings</span></span>

<span data-ttu-id="1c588-108">La **Access Connectivity Engine\\motores\\Excel** carpeta incluye la configuración de inicialización para el controlador Aceexcl.dll, utilizado para el acceso externo a hojas de cálculo de Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1c588-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="1c588-109">En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="1c588-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="1c588-110">El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Excel de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="1c588-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c588-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="1c588-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="1c588-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c588-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c588-113">Win32</span><span class="sxs-lookup"><span data-stu-id="1c588-113">win32</span></span></p></td>
<td><p><span data-ttu-id="1c588-p103">Ubicación de msexcl40.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="1c588-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c588-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="1c588-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="1c588-118">El número de filas que se puede comprobar el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c588-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="1c588-119">Se determina el tipo de datos dado el número máximo de tipos de datos que se encuentra.</span><span class="sxs-lookup"><span data-stu-id="1c588-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="1c588-120">Si no hay una placa, se determina el tipo de datos en el siguiente orden: número, moneda, fecha, texto, Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c588-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="1c588-121">Si se encuentran datos que no coincide con el tipo de datos estimado para la columna, se devuelve como un valor <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="1c588-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="1c588-122">En la importación, si una columna tiene distintos tipos de datos, se convertirá la columna entera según la configuración de ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="1c588-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="1c588-123">El número predeterminado de filas que se va a comprobar es 8.</span><span class="sxs-lookup"><span data-stu-id="1c588-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="1c588-124">Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="1c588-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c588-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="1c588-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="1c588-p105">Su valor se puede establecer en MajorityType o Text. Si se establece en MajorityType, las columnas con tipos de datos mixtos se convertirán al tipo de datos predominante en la importación. Si se establece como Text, las columnas con tipos de datos mixtos se convertirán a texto en la importación. El valor predeterminado es Text. Los valores son de tipo REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="1c588-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c588-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="1c588-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="1c588-p106">Número de filas en blanco que se deben agregar al final de una hoja de cálculo de la Versión 3.5 o 4.0 antes de que se agreguen nuevos datos. Por ejemplo, si se establece AppendBlankRows en 4, Microsoft Jet agregará 4 filas en blanco al final de la hoja de cálculo antes de agregar filas que contengan datos. Los valores enteros para esta configuración pueden oscilar entre 0 y 16; el valor predeterminado es 01 (se agrega una fila adicional). Los valores son de tipo REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="1c588-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c588-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="1c588-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="1c588-p107">Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila. Un valor de 00 indica que no hay nombres de columna en la primera fila; dichos nombres aparecerán como F1, F2, F3, etc. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="1c588-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c588-142">La **Access Connectivity Engine\\motores\\Excel 8.0** carpeta contiene las siguientes entradas, que se aplican a Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="1c588-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c588-143">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="1c588-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="1c588-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c588-144">Type</span></span></p></th>
<th><p><span data-ttu-id="1c588-145">Valor</span><span class="sxs-lookup"><span data-stu-id="1c588-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c588-146">Engine</span><span class="sxs-lookup"><span data-stu-id="1c588-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="1c588-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1c588-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1c588-148">Excel</span><span class="sxs-lookup"><span data-stu-id="1c588-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c588-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="1c588-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="1c588-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1c588-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1c588-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="1c588-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c588-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="1c588-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="1c588-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c588-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1c588-154">01</span><span class="sxs-lookup"><span data-stu-id="1c588-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c588-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="1c588-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="1c588-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c588-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1c588-157">00</span><span class="sxs-lookup"><span data-stu-id="1c588-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c588-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="1c588-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="1c588-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1c588-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="1c588-160">1</span><span class="sxs-lookup"><span data-stu-id="1c588-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c588-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="1c588-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="1c588-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c588-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1c588-163">00</span><span class="sxs-lookup"><span data-stu-id="1c588-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c588-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="1c588-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="1c588-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c588-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1c588-166">01</span><span class="sxs-lookup"><span data-stu-id="1c588-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c588-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="1c588-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="1c588-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1c588-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1c588-p108">Exportar datos de la base de datos activa a un archivo de Microsoft Excel 97. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</span><span class="sxs-lookup"><span data-stu-id="1c588-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c588-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="1c588-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="1c588-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c588-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1c588-173">01</span><span class="sxs-lookup"><span data-stu-id="1c588-173">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="1c588-174">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="1c588-174">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


