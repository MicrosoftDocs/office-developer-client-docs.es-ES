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
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="a3c1e-102">Índice de propiedades dinámicas de ADO</span><span class="sxs-lookup"><span data-stu-id="a3c1e-102">ADO dynamic property index</span></span>

<span data-ttu-id="a3c1e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3c1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3c1e-p101">Los proveedores de datos, servicios y los componentes de servicios pueden agregar propiedades dinámicas a las colecciones **Properties** de los objetos [Connection](connection-object-ado.md) y [Recordset](recordset-object-ado.md) sin abrir. Un proveedor determinado también puede insertar propiedades adicionales al abrir estos objetos. Algunas de estas propiedades se enumeran en la sección [Propiedades dinámicas de ADO](ado-dynamic-properties.md). Aparecen más bajo los proveedores concretos en la sección [Apéndice A: Proveedores](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="a3c1e-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="a3c1e-p102">La tabla siguiente es un índice cruzado de los nombres ADO y OLE DB de cada propiedad dinámica de proveedor OLE DB estándar. Los proveedores pueden agregar más propiedades a las enumeradas aquí. Para obtener información específica acerca de las propiedades dinámicas específicas de cada proveedor, vea la documentación del mismo.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="a3c1e-p103">La Referencia del programador de OLE DB hace referencia a un nombre de propiedad de ADO por el término, "Descripción". Puede buscar más información sobre estas propiedades estándar en la Referencia del programador de OLE DB. Busque el nombre de la propiedad de OLE DB en el índice o vea los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="a3c1e-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="a3c1e-114">Apéndice C: Propiedades de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a3c1e-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="a3c1e-115">Propiedades compatibles con el servicio de cursores</span><span class="sxs-lookup"><span data-stu-id="a3c1e-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="a3c1e-116">Propiedades compatibles con el proveedor de persistencia</span><span class="sxs-lookup"><span data-stu-id="a3c1e-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="a3c1e-117">Propiedades compatibles con el proveedor OLE DB de servicios remotos</span><span class="sxs-lookup"><span data-stu-id="a3c1e-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="a3c1e-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3c1e-118">Remarks</span></span>

<span data-ttu-id="a3c1e-119">Tenga en cuenta los números utilizados en el índice cruzado:</span><span class="sxs-lookup"><span data-stu-id="a3c1e-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="a3c1e-p104">(1) Esta propiedad es una marca booleana que indica si se debe usar la interfaz con nombre. El nombre de la propiedad de OLE DB equivalente aparece si existe.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="a3c1e-122">(2) La propiedad "Bookmarkable" ADO se genera internamente para la compatibilidad con versiones anteriores y se asigna a la propiedad OLE DB, DBPROP \_ IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="a3c1e-123">Se trata de la misma propiedad que corresponde a la propiedad ADO, IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="a3c1e-124">(3) El nombre de la propiedad ADO, "Hidden Columns", es distinto al de la propiedad de OLE DB, "Hidden Columns Count".</span><span class="sxs-lookup"><span data-stu-id="a3c1e-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="a3c1e-p106">(4) En los conjuntos de registros jerárquicos, la propiedad ADO "Maximum Rows" se aplica a todos los elementos secundarios. Según el orden en que se devuelvan las filas, en el conjunto de resultados pueden aparecer todos, algunos o ningún elemento secundario de cada elemento primario o incluso elementos secundarios huérfanos. Por lo tanto, al cambiar la forma de los conjuntos de registros jerárquicos, el identificador de cada elemento secundario debe ser exclusivo. En general, el proveedor del [Servicio de forma de datos de Microsoft para OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) no permite distinciones entre propiedades que se pueden heredar de un elemento primario y las que no se pueden heredar.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="a3c1e-129">(5) No aplicable.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-129">(5) Does not apply.</span></span>

<span data-ttu-id="a3c1e-130">**Propiedades dinámicas de Connection**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3c1e-131">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a3c1e-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a3c1e-132">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a3c1e-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="a3c1e-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="a3c1e-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="a3c1e-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a3c1e-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="a3c1e-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="a3c1e-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="a3c1e-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="a3c1e-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="a3c1e-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="a3c1e-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="a3c1e-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="a3c1e-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="a3c1e-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="a3c1e-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="a3c1e-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="a3c1e-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="a3c1e-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a3c1e-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="a3c1e-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="a3c1e-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="a3c1e-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="a3c1e-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="a3c1e-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="a3c1e-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="a3c1e-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="a3c1e-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="a3c1e-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="a3c1e-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="a3c1e-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="a3c1e-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="a3c1e-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="a3c1e-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="a3c1e-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="a3c1e-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="a3c1e-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-177">Ubicación</span><span class="sxs-lookup"><span data-stu-id="a3c1e-177">Location</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="a3c1e-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="a3c1e-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="a3c1e-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="a3c1e-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="a3c1e-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-187">Mode</span><span class="sxs-lookup"><span data-stu-id="a3c1e-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="a3c1e-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="a3c1e-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a3c1e-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="a3c1e-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="a3c1e-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="a3c1e-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="a3c1e-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a3c1e-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="a3c1e-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="a3c1e-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="a3c1e-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="a3c1e-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="a3c1e-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="a3c1e-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="a3c1e-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="a3c1e-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="a3c1e-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-215">Password</span><span class="sxs-lookup"><span data-stu-id="a3c1e-215">Password</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a3c1e-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="a3c1e-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="a3c1e-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="a3c1e-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="a3c1e-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a3c1e-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="a3c1e-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="a3c1e-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="a3c1e-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="a3c1e-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="a3c1e-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="a3c1e-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="a3c1e-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="a3c1e-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="a3c1e-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="a3c1e-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="a3c1e-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="a3c1e-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="a3c1e-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a3c1e-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="a3c1e-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="a3c1e-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="a3c1e-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="a3c1e-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="a3c1e-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="a3c1e-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="a3c1e-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="a3c1e-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="a3c1e-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="a3c1e-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="a3c1e-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-253">User ID</span><span class="sxs-lookup"><span data-stu-id="a3c1e-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="a3c1e-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-255">User Name</span><span class="sxs-lookup"><span data-stu-id="a3c1e-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="a3c1e-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="a3c1e-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="a3c1e-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3c1e-259">**Propiedades dinámicas de Recordset**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="a3c1e-260">Tenga en cuenta que las **propiedades dinámicas** del objeto **Recordset** se salen del ámbito (no están disponibles) cuando el objeto **Recordset** está cerrado.</span><span class="sxs-lookup"><span data-stu-id="a3c1e-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3c1e-261">Nombre de propiedad de ADO</span><span class="sxs-lookup"><span data-stu-id="a3c1e-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="a3c1e-262">Nombre de propiedad de OLE DB</span><span class="sxs-lookup"><span data-stu-id="a3c1e-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="a3c1e-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="a3c1e-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-266">(1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="a3c1e-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="a3c1e-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="a3c1e-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="a3c1e-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-274">(1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="a3c1e-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="a3c1e-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="a3c1e-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="a3c1e-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-282">(1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="a3c1e-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="a3c1e-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-286">(1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="a3c1e-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="a3c1e-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="a3c1e-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="a3c1e-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="a3c1e-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="a3c1e-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-298">(1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="a3c1e-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="a3c1e-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="a3c1e-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="a3c1e-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="a3c1e-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="a3c1e-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-311">IStream</span><span class="sxs-lookup"><span data-stu-id="a3c1e-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="a3c1e-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="a3c1e-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="a3c1e-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="a3c1e-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="a3c1e-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="a3c1e-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="a3c1e-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="a3c1e-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="a3c1e-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="a3c1e-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="a3c1e-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="a3c1e-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="a3c1e-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="a3c1e-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="a3c1e-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="a3c1e-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="a3c1e-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="a3c1e-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="a3c1e-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="a3c1e-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="a3c1e-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="a3c1e-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="a3c1e-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="a3c1e-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="a3c1e-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="a3c1e-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="a3c1e-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="a3c1e-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="a3c1e-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="a3c1e-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="a3c1e-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a3c1e-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="a3c1e-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="a3c1e-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="a3c1e-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="a3c1e-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="a3c1e-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="a3c1e-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="a3c1e-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a3c1e-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a3c1e-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="a3c1e-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="a3c1e-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="a3c1e-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="a3c1e-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-403">Private1</span><span class="sxs-lookup"><span data-stu-id="a3c1e-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-404">(5)</span><span class="sxs-lookup"><span data-stu-id="a3c1e-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="a3c1e-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="a3c1e-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="a3c1e-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="a3c1e-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="a3c1e-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="a3c1e-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="a3c1e-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="a3c1e-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="a3c1e-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a3c1e-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="a3c1e-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="a3c1e-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="a3c1e-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="a3c1e-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="a3c1e-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="a3c1e-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="a3c1e-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="a3c1e-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="a3c1e-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="a3c1e-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a3c1e-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="a3c1e-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="a3c1e-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="a3c1e-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="a3c1e-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="a3c1e-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="a3c1e-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="a3c1e-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="a3c1e-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="a3c1e-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="a3c1e-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="a3c1e-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="a3c1e-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="a3c1e-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3c1e-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="a3c1e-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="a3c1e-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3c1e-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="a3c1e-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="a3c1e-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="a3c1e-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

