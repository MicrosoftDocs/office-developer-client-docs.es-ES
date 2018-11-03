---
title: Códigos de error de DataControl
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fcb9a2cd456e09edc84475fb47c5cca8a548d561
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947766"
---
# <a name="datacontrol-error-codes"></a><span data-ttu-id="a1f41-102">Códigos de error de DataControl</span><span class="sxs-lookup"><span data-stu-id="a1f41-102">DataControl error codes</span></span>


<span data-ttu-id="a1f41-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1f41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1f41-p101">En la tabla siguiente se enumeran los códigos de error del objeto [RDS.DataControl](datacontrol-object-rds.md). Se muestra la traducción decimal positiva de los dos bytes inferiores, la traducción decimal negativa del código de error completo y los valores hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="a1f41-p101">The following table lists the [RDS.DataControl](datacontrol-object-rds.md) object error codes. The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1f41-106">Códigos de error de RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="a1f41-106">RDS.DataControl error codes</span></span></p></th>
<th><p><span data-ttu-id="a1f41-107">Número</span><span class="sxs-lookup"><span data-stu-id="a1f41-107">Number</span></span></p></th>
<th><p><span data-ttu-id="a1f41-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1f41-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-109"><strong>IDS_AsyncPending</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-109"><strong>IDS_AsyncPending</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-110">4107</span><span class="sxs-lookup"><span data-stu-id="a1f41-110">4107</span></span><br />
<span data-ttu-id="a1f41-111">-2146824175</span><span class="sxs-lookup"><span data-stu-id="a1f41-111">-2146824175</span></span><br />
<span data-ttu-id="a1f41-112">0x800A1011</span><span class="sxs-lookup"><span data-stu-id="a1f41-112">0x800A1011</span></span></p></td>
<td><p><span data-ttu-id="a1f41-113">No se puede efectuar la operación con una operación asíncrona pendiente.</span><span class="sxs-lookup"><span data-stu-id="a1f41-113">Operation cannot be performed while async operation is pending.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-114"><strong>IDS_BadInlineTablegram</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-114"><strong>IDS_BadInlineTablegram</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-115">4105</span><span class="sxs-lookup"><span data-stu-id="a1f41-115">4105</span></span><br />
<span data-ttu-id="a1f41-116">-2146824183</span><span class="sxs-lookup"><span data-stu-id="a1f41-116">-2146824183</span></span><br />
<span data-ttu-id="a1f41-117">0x800A1009</span><span class="sxs-lookup"><span data-stu-id="a1f41-117">0x800A1009</span></span></p></td>
<td><p><span data-ttu-id="a1f41-118">Tablegram en línea no válido.</span><span class="sxs-lookup"><span data-stu-id="a1f41-118">Bad inline tablegram.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-119"><strong>IDS_CantConnect</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-119"><strong>IDS_CantConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-120">4099</span><span class="sxs-lookup"><span data-stu-id="a1f41-120">4099</span></span><br />
<span data-ttu-id="a1f41-121">-2146824189</span><span class="sxs-lookup"><span data-stu-id="a1f41-121">-2146824189</span></span><br />
<span data-ttu-id="a1f41-122">0x800A1003</span><span class="sxs-lookup"><span data-stu-id="a1f41-122">0x800A1003</span></span></p></td>
<td><p><span data-ttu-id="a1f41-123">No se puede conectar al servidor.</span><span class="sxs-lookup"><span data-stu-id="a1f41-123">Cannot connect to server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-124"><strong>IDS_CantCreateObject</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-124"><strong>IDS_CantCreateObject</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-125">4100</span><span class="sxs-lookup"><span data-stu-id="a1f41-125">4100</span></span><br />
<span data-ttu-id="a1f41-126">-2146824188</span><span class="sxs-lookup"><span data-stu-id="a1f41-126">-2146824188</span></span><br />
<span data-ttu-id="a1f41-127">0x800A1004</span><span class="sxs-lookup"><span data-stu-id="a1f41-127">0x800A1004</span></span></p></td>
<td><p><span data-ttu-id="a1f41-128">No se puede crear el objeto de negocios.</span><span class="sxs-lookup"><span data-stu-id="a1f41-128">Business object cannot be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-129"><strong>IDS_CantFindDataspace</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-129"><strong>IDS_CantFindDataspace</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-130">4102</span><span class="sxs-lookup"><span data-stu-id="a1f41-130">4102</span></span><br />
<span data-ttu-id="a1f41-131">-2146824186</span><span class="sxs-lookup"><span data-stu-id="a1f41-131">-2146824186</span></span><br />
<span data-ttu-id="a1f41-132">0x800A1006</span><span class="sxs-lookup"><span data-stu-id="a1f41-132">0x800A1006</span></span></p></td>
<td><p><span data-ttu-id="a1f41-133">La propiedad Dataspace no es válida.</span><span class="sxs-lookup"><span data-stu-id="a1f41-133">Dataspace property is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-134"><strong>IDS_CantInvokeMethod</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-134"><strong>IDS_CantInvokeMethod</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-135">4101</span><span class="sxs-lookup"><span data-stu-id="a1f41-135">4101</span></span><br />
<span data-ttu-id="a1f41-136">-2146824187</span><span class="sxs-lookup"><span data-stu-id="a1f41-136">-2146824187</span></span><br />
<span data-ttu-id="a1f41-137">0x800A1005</span><span class="sxs-lookup"><span data-stu-id="a1f41-137">0x800A1005</span></span></p></td>
<td><p><span data-ttu-id="a1f41-138">No se puede invocar el método en el objeto de negocios.</span><span class="sxs-lookup"><span data-stu-id="a1f41-138">Method cannot be invoked on business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-139"><strong>IDS_CrossDomainWarning</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-139"><strong>IDS_CrossDomainWarning</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-140">4112</span><span class="sxs-lookup"><span data-stu-id="a1f41-140">4112</span></span><br />
<span data-ttu-id="a1f41-141">-2146824170</span><span class="sxs-lookup"><span data-stu-id="a1f41-141">-2146824170</span></span><br />
<span data-ttu-id="a1f41-142">0x800A1016</span><span class="sxs-lookup"><span data-stu-id="a1f41-142">0x800A1016</span></span></p></td>
<td><p><span data-ttu-id="a1f41-143">Esta página obtiene acceso a datos en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="a1f41-143">This page accesses data on another domain.</span></span> <span data-ttu-id="a1f41-144">¿Desea permitir esto?</span><span class="sxs-lookup"><span data-stu-id="a1f41-144">Do you want to allow this?</span></span> <span data-ttu-id="a1f41-145">Para evitar este mensaje en Internet Explorer, puede agregar un sitio Web seguro a la zona Sitios de confianza en la ficha <strong>seguridad</strong> del cuadro de diálogo <strong>Opciones de Internet</strong> .</span><span class="sxs-lookup"><span data-stu-id="a1f41-145">To avoid this message in Internet Explorer, you can add a secure website to your Trusted Sites zone on the <strong>Security</strong> tab of the <strong>Internet Options</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-146"><strong>IDS_InvalidADCClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-146"><strong>IDS_InvalidADCClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-147">4106</span><span class="sxs-lookup"><span data-stu-id="a1f41-147">4106</span></span><br />
<span data-ttu-id="a1f41-148">-2146824176</span><span class="sxs-lookup"><span data-stu-id="a1f41-148">-2146824176</span></span><br />
<span data-ttu-id="a1f41-149">0x800A1010</span><span class="sxs-lookup"><span data-stu-id="a1f41-149">0x800A1010</span></span></p></td>
<td><p><span data-ttu-id="a1f41-150">Versión de cliente de RDS no válida, El cliente es más reciente que el servidor.</span><span class="sxs-lookup"><span data-stu-id="a1f41-150">Invalid RDS Client Version — Client is newer than server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-151"><strong>IDS_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-151"><strong>IDS_INVALIDARG</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-152">5376</span><span class="sxs-lookup"><span data-stu-id="a1f41-152">5376</span></span><br />
<span data-ttu-id="a1f41-153">-2147019520</span><span class="sxs-lookup"><span data-stu-id="a1f41-153">-2147019520</span></span><br />
<span data-ttu-id="a1f41-154">0x80071500</span><span class="sxs-lookup"><span data-stu-id="a1f41-154">0x80071500</span></span></p></td>
<td><p><span data-ttu-id="a1f41-155">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a1f41-155">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-156"><strong>IDS_InvalidBindings</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-156"><strong>IDS_InvalidBindings</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-157">4097</span><span class="sxs-lookup"><span data-stu-id="a1f41-157">4097</span></span><br />
<span data-ttu-id="a1f41-158">-2146824191</span><span class="sxs-lookup"><span data-stu-id="a1f41-158">-2146824191</span></span><br />
<span data-ttu-id="a1f41-159">0x800A1001</span><span class="sxs-lookup"><span data-stu-id="a1f41-159">0x800A1001</span></span></p></td>
<td><p><span data-ttu-id="a1f41-160">Error en la propiedad de enlaces.</span><span class="sxs-lookup"><span data-stu-id="a1f41-160">Error in bindings property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-161"><strong>IDS_InvalidParam</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-161"><strong>IDS_InvalidParam</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-162">4110</span><span class="sxs-lookup"><span data-stu-id="a1f41-162">4110</span></span><br />
<span data-ttu-id="a1f41-163">-2146824172</span><span class="sxs-lookup"><span data-stu-id="a1f41-163">-2146824172</span></span><br />
<span data-ttu-id="a1f41-164">0x800A1014</span><span class="sxs-lookup"><span data-stu-id="a1f41-164">0x800A1014</span></span></p></td>
<td><p><span data-ttu-id="a1f41-165">Uno o más argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a1f41-165">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-166"><strong>IDS_NOINTERFACE</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-166"><strong>IDS_NOINTERFACE</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-167">5377</span><span class="sxs-lookup"><span data-stu-id="a1f41-167">5377</span></span><br />
<span data-ttu-id="a1f41-168">-2147019519</span><span class="sxs-lookup"><span data-stu-id="a1f41-168">-2147019519</span></span><br />
<span data-ttu-id="a1f41-169">0x80071501</span><span class="sxs-lookup"><span data-stu-id="a1f41-169">0x80071501</span></span></p></td>
<td><p><span data-ttu-id="a1f41-170">Interfaz no compatible.</span><span class="sxs-lookup"><span data-stu-id="a1f41-170">No such interface is supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-171"><strong>IDS_NotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-171"><strong>IDS_NotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-172">4111</span><span class="sxs-lookup"><span data-stu-id="a1f41-172">4111</span></span><br />
<span data-ttu-id="a1f41-173">-2146824171</span><span class="sxs-lookup"><span data-stu-id="a1f41-173">-2146824171</span></span><br />
<span data-ttu-id="a1f41-174">0x800A1015</span><span class="sxs-lookup"><span data-stu-id="a1f41-174">0x800A1015</span></span></p></td>
<td><p><span data-ttu-id="a1f41-175">La petición no se puede ejecutar mientras el controlador de eventos esté procesando.</span><span class="sxs-lookup"><span data-stu-id="a1f41-175">Request cannot be executed while the event handler is still processing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-176"><strong>IDS_ObjectNotSafe</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-176"><strong>IDS_ObjectNotSafe</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-177">4103</span><span class="sxs-lookup"><span data-stu-id="a1f41-177">4103</span></span><br />
<span data-ttu-id="a1f41-178">-2146824185</span><span class="sxs-lookup"><span data-stu-id="a1f41-178">-2146824185</span></span><br />
<span data-ttu-id="a1f41-179">0x800A1007</span><span class="sxs-lookup"><span data-stu-id="a1f41-179">0x800A1007</span></span></p></td>
<td><p><span data-ttu-id="a1f41-180">La configuración de seguridad de este equipo prohíbe la creación de objetos de negocio.</span><span class="sxs-lookup"><span data-stu-id="a1f41-180">Safety settings on this computer prohibit creation of business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-181"><strong>IDS_RecordsetNotOpen</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-181"><strong>IDS_RecordsetNotOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-182">4109</span><span class="sxs-lookup"><span data-stu-id="a1f41-182">4109</span></span><br />
<span data-ttu-id="a1f41-183">-2146824173</span><span class="sxs-lookup"><span data-stu-id="a1f41-183">-2146824173</span></span><br />
<span data-ttu-id="a1f41-184">0x800A1013</span><span class="sxs-lookup"><span data-stu-id="a1f41-184">0x800A1013</span></span></p></td>
<td><p><span data-ttu-id="a1f41-185"><strong>Recordset</strong> no abierto.</span><span class="sxs-lookup"><span data-stu-id="a1f41-185"><strong>Recordset</strong> is not open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-186"><strong>IDS_ResetInvalidField</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-186"><strong>IDS_ResetInvalidField</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-187">4108</span><span class="sxs-lookup"><span data-stu-id="a1f41-187">4108</span></span><br />
<span data-ttu-id="a1f41-188">-2146824174</span><span class="sxs-lookup"><span data-stu-id="a1f41-188">-2146824174</span></span><br />
<span data-ttu-id="a1f41-189">0x800A1012</span><span class="sxs-lookup"><span data-stu-id="a1f41-189">0x800A1012</span></span></p></td>
<td><p><span data-ttu-id="a1f41-190">La columna especificada en <strong>SortColumn</strong> o <strong>FilterColumn</strong> no existe.</span><span class="sxs-lookup"><span data-stu-id="a1f41-190">Column specified in <strong>SortColumn</strong> or <strong>FilterColumn</strong> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-191"><strong>IDS_RowsetNotUpdateable</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-191"><strong>IDS_RowsetNotUpdateable</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-192">4104</span><span class="sxs-lookup"><span data-stu-id="a1f41-192">4104</span></span><br />
<span data-ttu-id="a1f41-193">-2146824184</span><span class="sxs-lookup"><span data-stu-id="a1f41-193">-2146824184</span></span><br />
<span data-ttu-id="a1f41-194">0x800A1008</span><span class="sxs-lookup"><span data-stu-id="a1f41-194">0x800A1008</span></span></p></td>
<td><p><span data-ttu-id="a1f41-195">No se puede actualizar el conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="a1f41-195">Rowset not updateable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-196"><strong>IDS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-196"><strong>IDS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-197">4351</span><span class="sxs-lookup"><span data-stu-id="a1f41-197">4351</span></span><br />
<span data-ttu-id="a1f41-198">-2146823937</span><span class="sxs-lookup"><span data-stu-id="a1f41-198">-2146823937</span></span><br />
<span data-ttu-id="a1f41-199">0x800A10FF</span><span class="sxs-lookup"><span data-stu-id="a1f41-199">0x800A10FF</span></span></p></td>
<td><p><span data-ttu-id="a1f41-200">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a1f41-200">Unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1f41-201"><strong>IDS_UpdatesFailed</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-201"><strong>IDS_UpdatesFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-202">4098</span><span class="sxs-lookup"><span data-stu-id="a1f41-202">4098</span></span><br />
<span data-ttu-id="a1f41-203">-2146824190</span><span class="sxs-lookup"><span data-stu-id="a1f41-203">-2146824190</span></span><br />
<span data-ttu-id="a1f41-204">0x800A1002</span><span class="sxs-lookup"><span data-stu-id="a1f41-204">0x800A1002</span></span></p></td>
<td><p><span data-ttu-id="a1f41-205">No se puede actualizar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a1f41-205">Unable to update database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1f41-206"><strong>IDS_URLMONNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="a1f41-206"><strong>IDS_URLMONNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="a1f41-207">4119</span><span class="sxs-lookup"><span data-stu-id="a1f41-207">4119</span></span><br />
<span data-ttu-id="a1f41-208">-2146824169</span><span class="sxs-lookup"><span data-stu-id="a1f41-208">-2146824169</span></span><br />
<span data-ttu-id="a1f41-209">0x800A1017</span><span class="sxs-lookup"><span data-stu-id="a1f41-209">0x800A1017</span></span></p></td>
<td><p><span data-ttu-id="a1f41-210">La propiedad <strong>URL</strong> de DataControl necesita el archivo del sistema Urlmon.dll, pero no se puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="a1f41-210">DataControl <strong>URL</strong> property requires the system file Urlmon.dll, which cannot be found.</span></span></p></td>
</tr>
</tbody>
</table>

