---
title: Inicializar el controlador de origen de datos de Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 39cad98bc6f14509491e78ac4057d6488528f0b4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947857"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="0219b-102">Inicializar el controlador de origen de datos de Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0219b-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="0219b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0219b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0219b-104">Al instalar el controlador de orígenes de datos de Microsoft Exchange, el programa de instalación escribe un conjunto de valores predeterminados en el registro de Windows de Microsoft en las subclaves de los motores y los formatos ISAM.</span><span class="sxs-lookup"><span data-stu-id="0219b-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="0219b-105">No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0219b-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="0219b-106">Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de orígenes de datos de Microsoft® Exchange.</span><span class="sxs-lookup"><span data-stu-id="0219b-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="0219b-107">Configuración de inicialización del origen de datos de Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0219b-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="0219b-108">La **Access Connectivity Engine\\motores\\Exchange** carpeta incluye la configuración de inicialización para el controlador Aceexch.dll, utilizado para el acceso externo a las carpetas de Microsoft Outlook y Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="0219b-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="0219b-109">La única entrada de esta carpeta es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="0219b-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="0219b-110">El motor de base de datos de Microsoft Access utiliza este valor para indicar la ubicación de Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="0219b-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="0219b-111">La ruta de acceso completa se determina durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0219b-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="0219b-112">Los valores son de tipo REG\_SZ.</span><span class="sxs-lookup"><span data-stu-id="0219b-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="0219b-p104">Los resultados de utilizar el formato ISAM de Outlook y el formato ISAM del cliente de Exchange son similares. La única diferencia estriba en que los dos clientes utilizan nombres distintos para las mismas columnas. Ambos formatos ISAM se han creado con objeto de que el motor de base de datos de Microsoft Access pueda devolver los nombres de las columnas en el estilo determinado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0219b-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="0219b-116">Formatos ISAM del cliente de Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="0219b-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="0219b-117">La **Access Connectivity Engine\\formatos ISAM de\\Outlook 9.0** carpeta contiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="0219b-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0219b-118">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="0219b-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="0219b-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="0219b-119">Type</span></span></p></th>
<th><p><span data-ttu-id="0219b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0219b-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0219b-121">Engine</span><span class="sxs-lookup"><span data-stu-id="0219b-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="0219b-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0219b-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0219b-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="0219b-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="0219b-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="0219b-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0219b-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0219b-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="0219b-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0219b-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="0219b-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="0219b-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-129">01</span><span class="sxs-lookup"><span data-stu-id="0219b-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="0219b-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="0219b-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-132">00</span><span class="sxs-lookup"><span data-stu-id="0219b-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0219b-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="0219b-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="0219b-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0219b-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="0219b-135">3</span><span class="sxs-lookup"><span data-stu-id="0219b-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="0219b-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="0219b-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-138">00</span><span class="sxs-lookup"><span data-stu-id="0219b-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0219b-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="0219b-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="0219b-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-141">00</span><span class="sxs-lookup"><span data-stu-id="0219b-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="0219b-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="0219b-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-144">01</span><span class="sxs-lookup"><span data-stu-id="0219b-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="0219b-145">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="0219b-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="0219b-146">Formatos ISAM del cliente de Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="0219b-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="0219b-147">La **Access Connectivity Engine\\formatos ISAM de\\Exchange 4.0** carpeta contiene las siguientes entradas.</span><span class="sxs-lookup"><span data-stu-id="0219b-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0219b-148">Nombre de la entrada</span><span class="sxs-lookup"><span data-stu-id="0219b-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="0219b-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="0219b-149">Type</span></span></p></th>
<th><p><span data-ttu-id="0219b-150">Valor</span><span class="sxs-lookup"><span data-stu-id="0219b-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0219b-151">Engine</span><span class="sxs-lookup"><span data-stu-id="0219b-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="0219b-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0219b-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0219b-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="0219b-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="0219b-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="0219b-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="0219b-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="0219b-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="0219b-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0219b-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="0219b-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="0219b-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-159">01</span><span class="sxs-lookup"><span data-stu-id="0219b-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="0219b-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="0219b-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-162">00</span><span class="sxs-lookup"><span data-stu-id="0219b-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0219b-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="0219b-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="0219b-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="0219b-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="0219b-165">3</span><span class="sxs-lookup"><span data-stu-id="0219b-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="0219b-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="0219b-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-168">00</span><span class="sxs-lookup"><span data-stu-id="0219b-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0219b-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="0219b-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="0219b-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-171">00</span><span class="sxs-lookup"><span data-stu-id="0219b-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0219b-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="0219b-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="0219b-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="0219b-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="0219b-174">01</span><span class="sxs-lookup"><span data-stu-id="0219b-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="0219b-175">Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="0219b-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="0219b-176">Personalizar el archivo Schema.ini para los datos de Outlook y de Exchange</span><span class="sxs-lookup"><span data-stu-id="0219b-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="0219b-p105">Outlook y Exchange utilizan el archivo Schema.ini casi de la misma manera que el ISAM de texto. Dicho archivo contiene los detalles de un origen de datos: cómo se da formato a los datos y los nombres de las columnas a las que se debe tener acceso.</span><span class="sxs-lookup"><span data-stu-id="0219b-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="0219b-p106">No es necesario modificarlo para poder leer, importar o exportar datos para Outlook y Exchange. Muchos de los valores incluidos en él para Outlook y Exchange son específicos de etiquetas internas requeridas por MAPI. No debe intentar modificar dichos valores de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="0219b-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

