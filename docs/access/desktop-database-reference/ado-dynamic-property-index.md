---
title: Índice de propiedades dinámicas de ADO
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bfe788923d623300edac28f0f27534b3ffd8b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283404"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="3fc2d-102">Índice de propiedades dinámicas de ADO</span><span class="sxs-lookup"><span data-stu-id="3fc2d-102">ADO dynamic property index</span></span>

<span data-ttu-id="3fc2d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fc2d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fc2d-p101">Los proveedores de datos, servicios y los componentes de servicios pueden agregar propiedades dinámicas a las colecciones **Properties** de los objetos [Connection](connection-object-ado.md) y [Recordset](recordset-object-ado.md) sin abrir. Un proveedor determinado también puede insertar propiedades adicionales al abrir estos objetos. Algunas de estas propiedades se enumeran en la sección [Propiedades dinámicas de ADO](ado-dynamic-properties.md). Aparecen más bajo los proveedores concretos en la sección [Apéndice A: Proveedores](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="3fc2d-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="3fc2d-p102">La tabla siguiente es un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica de proveedor OLE DB estándar. Los proveedores pueden agregar más propiedades a las enumeradas aquí. Para obtener información específica acerca de las propiedades dinámicas específicas de cada proveedor, vea la documentación del mismo.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="3fc2d-p103">La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades estándar en la Referencia del programador de OLE DB. Busque el nombre de la propiedad de OLE DB en el índice o vea los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="3fc2d-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="3fc2d-114">Apéndice C: Propiedades de OLE DB</span><span class="sxs-lookup"><span data-stu-id="3fc2d-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="3fc2d-115">Propiedades compatibles con el servicio de cursores</span><span class="sxs-lookup"><span data-stu-id="3fc2d-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="3fc2d-116">Propiedades compatibles con el proveedor de persistencia</span><span class="sxs-lookup"><span data-stu-id="3fc2d-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="3fc2d-117">Propiedades compatibles con el proveedor OLE DB de servicios remotos</span><span class="sxs-lookup"><span data-stu-id="3fc2d-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc2d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fc2d-118">Remarks</span></span>

<span data-ttu-id="3fc2d-119">Tenga en cuenta los números utilizados en el índice cruzado:</span><span class="sxs-lookup"><span data-stu-id="3fc2d-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="3fc2d-p104">(1) Esta propiedad es una marca booleana que indica si se debe usar la interfaz con nombre. El nombre de la propiedad de OLE DB equivalente aparece si existe.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="3fc2d-122">(2) La propiedad "Bookmarkable" ADO se genera internamente para la compatibilidad con versiones anteriores y se asigna a la propiedad OLE DB, DBPROP \_ IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="3fc2d-123">Se trata de la misma propiedad que corresponde a la propiedad ADO, IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="3fc2d-124">(3) El nombre de la propiedad ADO, "Hidden Columns", es distinto al de la propiedad de OLE DB, "Hidden Columns Count".</span><span class="sxs-lookup"><span data-stu-id="3fc2d-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="3fc2d-p106">(4) En los conjuntos de registros jerárquicos, la propiedad ADO "Maximum Rows" se aplica a todos los elementos secundarios. Según el orden en que se devuelvan las filas, en el conjunto de resultados pueden aparecer todos, algunos o ningún elemento secundario de cada elemento primario o incluso elementos secundarios huérfanos. Por lo tanto, al cambiar la forma de los conjuntos de registros jerárquicos, el identificador de cada elemento secundario debe ser exclusivo. En general, el proveedor del [Servicio de forma de datos de Microsoft para OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) no permite distinciones entre propiedades que se pueden heredar de un elemento primario y las que no se pueden heredar.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="3fc2d-129">(5) No aplicable.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-129">(5) Does not apply.</span></span>

<span data-ttu-id="3fc2d-130">**Propiedades dinámicas de Connection**</span><span class="sxs-lookup"><span data-stu-id="3fc2d-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fc2d-131">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="3fc2d-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3fc2d-132">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="3fc2d-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="3fc2d-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="3fc2d-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="3fc2d-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="3fc2d-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="3fc2d-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="3fc2d-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="3fc2d-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="3fc2d-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="3fc2d-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="3fc2d-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="3fc2d-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="3fc2d-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="3fc2d-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="3fc2d-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="3fc2d-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="3fc2d-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="3fc2d-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3fc2d-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="3fc2d-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="3fc2d-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="3fc2d-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="3fc2d-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="3fc2d-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="3fc2d-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="3fc2d-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="3fc2d-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="3fc2d-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="3fc2d-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="3fc2d-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3fc2d-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="3fc2d-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="3fc2d-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="3fc2d-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="3fc2d-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="3fc2d-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-177">Ubicación</span><span class="sxs-lookup"><span data-stu-id="3fc2d-177">Location</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="3fc2d-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="3fc2d-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="3fc2d-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="3fc2d-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="3fc2d-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-187">Mode</span><span class="sxs-lookup"><span data-stu-id="3fc2d-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="3fc2d-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="3fc2d-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3fc2d-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="3fc2d-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="3fc2d-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="3fc2d-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="3fc2d-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3fc2d-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="3fc2d-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="3fc2d-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="3fc2d-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="3fc2d-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="3fc2d-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="3fc2d-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="3fc2d-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="3fc2d-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="3fc2d-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-215">Password</span><span class="sxs-lookup"><span data-stu-id="3fc2d-215">Password</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="3fc2d-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="3fc2d-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="3fc2d-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="3fc2d-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="3fc2d-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3fc2d-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="3fc2d-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3fc2d-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="3fc2d-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="3fc2d-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="3fc2d-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="3fc2d-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="3fc2d-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="3fc2d-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="3fc2d-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="3fc2d-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="3fc2d-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="3fc2d-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="3fc2d-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="3fc2d-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="3fc2d-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="3fc2d-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="3fc2d-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="3fc2d-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="3fc2d-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="3fc2d-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="3fc2d-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="3fc2d-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="3fc2d-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="3fc2d-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="3fc2d-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-253">User ID</span><span class="sxs-lookup"><span data-stu-id="3fc2d-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="3fc2d-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-255">User Name</span><span class="sxs-lookup"><span data-stu-id="3fc2d-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="3fc2d-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="3fc2d-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="3fc2d-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fc2d-259">**Propiedades dinámicas de Recordset**</span><span class="sxs-lookup"><span data-stu-id="3fc2d-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="3fc2d-260">Tenga en cuenta que las **propiedades dinámicas** del objeto **Recordset** se salen del ámbito (no están disponibles) cuando el objeto **Recordset** está cerrado.</span><span class="sxs-lookup"><span data-stu-id="3fc2d-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fc2d-261">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="3fc2d-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3fc2d-262">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="3fc2d-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="3fc2d-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="3fc2d-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-266">(1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="3fc2d-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="3fc2d-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="3fc2d-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="3fc2d-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-274">(1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="3fc2d-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="3fc2d-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="3fc2d-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="3fc2d-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-282">(1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="3fc2d-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="3fc2d-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-286">(1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="3fc2d-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="3fc2d-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="3fc2d-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="3fc2d-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="3fc2d-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="3fc2d-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-298">(1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="3fc2d-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="3fc2d-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="3fc2d-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="3fc2d-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="3fc2d-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="3fc2d-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-311">IStream</span><span class="sxs-lookup"><span data-stu-id="3fc2d-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="3fc2d-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="3fc2d-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="3fc2d-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="3fc2d-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="3fc2d-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="3fc2d-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="3fc2d-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="3fc2d-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="3fc2d-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="3fc2d-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="3fc2d-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3fc2d-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="3fc2d-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="3fc2d-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="3fc2d-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="3fc2d-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="3fc2d-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="3fc2d-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="3fc2d-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="3fc2d-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="3fc2d-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="3fc2d-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="3fc2d-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="3fc2d-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="3fc2d-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="3fc2d-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="3fc2d-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="3fc2d-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="3fc2d-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="3fc2d-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="3fc2d-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3fc2d-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="3fc2d-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="3fc2d-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="3fc2d-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="3fc2d-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="3fc2d-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="3fc2d-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="3fc2d-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3fc2d-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3fc2d-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3fc2d-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3fc2d-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="3fc2d-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="3fc2d-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-403">Private1</span><span class="sxs-lookup"><span data-stu-id="3fc2d-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-404">(5)</span><span class="sxs-lookup"><span data-stu-id="3fc2d-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="3fc2d-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="3fc2d-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="3fc2d-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="3fc2d-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="3fc2d-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="3fc2d-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="3fc2d-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="3fc2d-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="3fc2d-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="3fc2d-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="3fc2d-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="3fc2d-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="3fc2d-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="3fc2d-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3fc2d-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="3fc2d-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="3fc2d-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="3fc2d-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="3fc2d-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="3fc2d-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3fc2d-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="3fc2d-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="3fc2d-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="3fc2d-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="3fc2d-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="3fc2d-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="3fc2d-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="3fc2d-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="3fc2d-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="3fc2d-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="3fc2d-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="3fc2d-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="3fc2d-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="3fc2d-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fc2d-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="3fc2d-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="3fc2d-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fc2d-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3fc2d-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3fc2d-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3fc2d-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

