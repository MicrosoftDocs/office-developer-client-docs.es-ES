---
title: SchemaEnum (referencia de base de datos de escritorio de Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308866"
---
# <a name="schemaenum"></a><span data-ttu-id="fe56a-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="fe56a-102">SchemaEnum</span></span>

<span data-ttu-id="fe56a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe56a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe56a-104">Especifica el tipo de esquema **Recordset** recuperado por el método [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fe56a-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe56a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe56a-105">Remarks</span></span>

<span data-ttu-id="fe56a-106">Se puede encontrar información adicional acerca de la función y las columnas que se devuelven para cada constante de ADO en los temas del Apéndice B de la *Referencia para programadores de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="fe56a-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="fe56a-107">El nombre de cada tema aparece entre paréntesis en la sección Descripción de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe56a-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="fe56a-108">Se puede encontrar información adicional acerca de la función y las columnas que se devuelven para cada constante ADO MD en los temas del Capítulo 23 de la documentación de *OLE DB para OLAP*.</span><span class="sxs-lookup"><span data-stu-id="fe56a-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="fe56a-109">El nombre de cada tema aparece entre paréntesis y se marca con un asterisco ( ) en la columna Descripción \* de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe56a-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="fe56a-110">Convierta los tipos de datos de columnas de la documentación de OLE DB a tipo de datos ADO consultando la columna Descripción del tema [DataTypeEnum](datatypeenum.md) de ADO.</span><span class="sxs-lookup"><span data-stu-id="fe56a-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="fe56a-111">Por ejemplo, un tipo de datos OLE DB **de DBTYPE \_ WSTR** equivale a un tipo de datos ADO **de adWChar**.</span><span class="sxs-lookup"><span data-stu-id="fe56a-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="fe56a-112">ADO genera resultados con el aspecto del esquema para las constantes **adSchemaDBInfoKeywords** y **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="fe56a-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="fe56a-113">ADO crea un conjunto de registros y, **a** continuación, rellena cada fila con los valores devueltos respectivamente por los métodos **IDBInfo::GetKeywords** e **IDBInfo::GetLiteralInfo.**</span><span class="sxs-lookup"><span data-stu-id="fe56a-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="fe56a-114">Puede encontrar información adicional acerca de estos métodos en la sección IDBInfo de la referencia del programador *de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="fe56a-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe56a-115">Constante</span><span class="sxs-lookup"><span data-stu-id="fe56a-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="fe56a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fe56a-116">Value</span></span></p></th>
<th><p><span data-ttu-id="fe56a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe56a-117">Description</span></span></p></th>
<th><p><span data-ttu-id="fe56a-118">Columnas de restricción</span><span class="sxs-lookup"><span data-stu-id="fe56a-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-120">0</span><span class="sxs-lookup"><span data-stu-id="fe56a-120">0</span></span></p></td>
<td><p><span data-ttu-id="fe56a-121">Devuelve las aserciones definidas en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-122">(Conjunto de filas ASSERTIONS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="fe56a-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-127">1 </span><span class="sxs-lookup"><span data-stu-id="fe56a-127">1</span></span></p></td>
<td><p><span data-ttu-id="fe56a-128">Devuelve los atributos físicos asociados con catálogos accesibles del sistema de administración de bases de datos (DBMS).</span><span class="sxs-lookup"><span data-stu-id="fe56a-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="fe56a-129">(Conjunto de filas CATALOGS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-132">2 </span><span class="sxs-lookup"><span data-stu-id="fe56a-132">2</span></span></p></td>
<td><p><span data-ttu-id="fe56a-133">Devuelve los conjuntos de caracteres definidos en el catálogo a los que puede tener acceso un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="fe56a-134">(Conjunto de filas CHARACTER_SETS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="fe56a-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-139">5 </span><span class="sxs-lookup"><span data-stu-id="fe56a-139">5</span></span></p></td>
<td><p><span data-ttu-id="fe56a-140">Devuelve las restricciones de comprobación definidas en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-141">(Conjunto de filas CHECK_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="fe56a-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-146">3 </span><span class="sxs-lookup"><span data-stu-id="fe56a-146">3</span></span></p></td>
<td><p><span data-ttu-id="fe56a-147">Devuelve las intercalaciones de caracteres definidas en el catálogo a las que puede tener acceso un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="fe56a-148">(Conjunto de filas COLLATIONS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="fe56a-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-153">13 </span><span class="sxs-lookup"><span data-stu-id="fe56a-153">13</span></span></p></td>
<td><p><span data-ttu-id="fe56a-154">Devuelve los privilegios sobre columnas de tablas que se definen en el catálogo y que están disponibles para (o los concede) un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="fe56a-155">(Conjunto de filas COLUMN_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-158">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="fe56a-160">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="fe56a-160">GRANTOR</span></span><br />
<span data-ttu-id="fe56a-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="fe56a-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-163">4 </span><span class="sxs-lookup"><span data-stu-id="fe56a-163">4</span></span></p></td>
<td><p><span data-ttu-id="fe56a-164">Devuelve las columnas de tablas (incluidas las vistas) definidas en el catálogo a las que puede tener acceso un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="fe56a-165">(Conjunto de filas COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-168">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-171">11</span><span class="sxs-lookup"><span data-stu-id="fe56a-171">11</span></span></p></td>
<td><p><span data-ttu-id="fe56a-172">Devuelve las columnas definidas en el catálogo que dependen de un dominio definido en el catálogo y pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="fe56a-173">(Conjunto de filas COLUMN_DOMAIN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="fe56a-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="fe56a-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="fe56a-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-179">6 </span><span class="sxs-lookup"><span data-stu-id="fe56a-179">6</span></span></p></td>
<td><p><span data-ttu-id="fe56a-180">Devuelve las columnas utilizadas por restricciones referenciales, restricciones de exclusividad, restricciones de comprobación y aserciones definidas en el catálogo y que son propiedad de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="fe56a-181">(Conjunto de filas CONSTRAINT_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="fe56a-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-184">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-187">7 </span><span class="sxs-lookup"><span data-stu-id="fe56a-187">7</span></span></p></td>
<td><p><span data-ttu-id="fe56a-188">Devuelve las tablas utilizadas por restricciones referenciales, restricciones de exclusividad, restricciones de comprobación y aserciones definidas en el catálogo y que son propiedad de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="fe56a-189">(Conjunto de filas CONSTRAINT_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="fe56a-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-194">32</span><span class="sxs-lookup"><span data-stu-id="fe56a-194">32</span></span></p></td>
<td><p><span data-ttu-id="fe56a-195">Devuelve información acerca de los cubos disponibles en un esquema (o en el catálogo, si el proveedor no admite esquemas).</span><span class="sxs-lookup"><span data-stu-id="fe56a-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="fe56a-196">(Conjunto de filas CUBE\*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-201">30</span><span class="sxs-lookup"><span data-stu-id="fe56a-201">30</span></span></p></td>
<td><p><span data-ttu-id="fe56a-202">Devuelve una lista de palabras clave específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fe56a-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="fe56a-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-204">&lt;Ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="fe56a-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-206">31</span><span class="sxs-lookup"><span data-stu-id="fe56a-206">31</span></span></p></td>
<td><p><span data-ttu-id="fe56a-207">Devuelve una lista de los literales específicos del proveedor utilizados en comandos de texto.</span><span class="sxs-lookup"><span data-stu-id="fe56a-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="fe56a-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-209">&lt;Ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="fe56a-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-211">33</span><span class="sxs-lookup"><span data-stu-id="fe56a-211">33</span></span></p></td>
<td><p><span data-ttu-id="fe56a-212">Devuelve información acerca de las dimensiones de un cubo dado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="fe56a-213">Tiene una fila para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="fe56a-213">It has one row for each dimension.</span></span> <span data-ttu-id="fe56a-214">(Conjunto de filas DIMENSIONS \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-217">CUBE_NAME</span></span><br />
<span data-ttu-id="fe56a-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="fe56a-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-221">27</span><span class="sxs-lookup"><span data-stu-id="fe56a-221">27</span></span></p></td>
<td><p><span data-ttu-id="fe56a-222">Devuelve las columnas de clave externa definidas por un usuario determinado en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="fe56a-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="fe56a-223">(Conjunto de filas FOREIGN_KEYS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-231">34</span><span class="sxs-lookup"><span data-stu-id="fe56a-231">34</span></span></p></td>
<td><p><span data-ttu-id="fe56a-232">Devuelve información acerca de las jerarquías disponibles en una dimensión.</span><span class="sxs-lookup"><span data-stu-id="fe56a-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="fe56a-233">(Conjunto de filas HIERARCHIES \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-236">CUBE_NAME</span></span><br />
<span data-ttu-id="fe56a-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="fe56a-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-241">12 </span><span class="sxs-lookup"><span data-stu-id="fe56a-241">12</span></span></p></td>
<td><p><span data-ttu-id="fe56a-242">Devuelve los índices definidos en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-243">(Conjunto de filas INDEXES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-246">INDEX_NAME</span></span><br />
<span data-ttu-id="fe56a-247">TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-247">TYPE</span></span><br />
<span data-ttu-id="fe56a-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-250">8 </span><span class="sxs-lookup"><span data-stu-id="fe56a-250">8</span></span></p></td>
<td><p><span data-ttu-id="fe56a-251">Devuelve las columnas definidas en el catálogo restringidas por un usuario determinado como claves.</span><span class="sxs-lookup"><span data-stu-id="fe56a-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="fe56a-252">(Conjunto de filas KEY_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="fe56a-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="fe56a-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="fe56a-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-258">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-261">35</span><span class="sxs-lookup"><span data-stu-id="fe56a-261">35</span></span></p></td>
<td><p><span data-ttu-id="fe56a-262">Devuelve información acerca de los niveles disponibles en una dimensión.</span><span class="sxs-lookup"><span data-stu-id="fe56a-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="fe56a-263">(Conjunto de filas LEVELS \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-266">CUBE_NAME</span></span><br />
<span data-ttu-id="fe56a-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="fe56a-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-272">36</span><span class="sxs-lookup"><span data-stu-id="fe56a-272">36</span></span></p></td>
<td><p><span data-ttu-id="fe56a-273">Devuelve información acerca de las medidas disponibles.</span><span class="sxs-lookup"><span data-stu-id="fe56a-273">Returns information about the available measures.</span></span> <span data-ttu-id="fe56a-274">(Conjunto de filas MEASURES \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-277">CUBE_NAME</span></span><br />
<span data-ttu-id="fe56a-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="fe56a-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-281">38</span><span class="sxs-lookup"><span data-stu-id="fe56a-281">38</span></span></p></td>
<td><p><span data-ttu-id="fe56a-282">Devuelve información acerca de los miembros disponibles.</span><span class="sxs-lookup"><span data-stu-id="fe56a-282">Returns information about the available members.</span></span> <span data-ttu-id="fe56a-283">(Conjunto de filas MEMBERS \*)</span><span class="sxs-lookup"><span data-stu-id="fe56a-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-286">CUBE_NAME</span></span><br />
<span data-ttu-id="fe56a-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="fe56a-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="fe56a-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="fe56a-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="fe56a-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="fe56a-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="fe56a-295">Operador de árbol (para obtener más información, vea la documentación de OLE DB para OLAP).</span><span class="sxs-lookup"><span data-stu-id="fe56a-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-297">28</span><span class="sxs-lookup"><span data-stu-id="fe56a-297">28</span></span></p></td>
<td><p><span data-ttu-id="fe56a-298">Devuelve las columnas de clave principal definidas por un usuario determinado en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="fe56a-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="fe56a-299">(Conjunto de filas PRIMARY_KEYS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-304">29</span><span class="sxs-lookup"><span data-stu-id="fe56a-304">29</span></span></p></td>
<td><p><span data-ttu-id="fe56a-305">Devuelve información acerca de las columnas de conjuntos de filas devueltos por procedimientos.</span><span class="sxs-lookup"><span data-stu-id="fe56a-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="fe56a-306">(Conjunto de filas PROCEDURE_COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="fe56a-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-312">26</span><span class="sxs-lookup"><span data-stu-id="fe56a-312">26</span></span></p></td>
<td><p><span data-ttu-id="fe56a-313">Devuelve información acerca de los parámetros y códigos de retorno de procedimientos.</span><span class="sxs-lookup"><span data-stu-id="fe56a-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="fe56a-314">(Conjunto de filas PROCEDURE_PARAMETERS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="fe56a-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-320">16 </span><span class="sxs-lookup"><span data-stu-id="fe56a-320">16</span></span></p></td>
<td><p><span data-ttu-id="fe56a-321">Devuelve los procedimientos definidos en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-322">(Conjunto de filas PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="fe56a-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-328">37</span><span class="sxs-lookup"><span data-stu-id="fe56a-328">37</span></span></p></td>
<td><p><span data-ttu-id="fe56a-329">Devuelve información acerca de las propiedades disponibles para cada nivel de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="fe56a-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="fe56a-330">(Conjunto de filas PROPERTIES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-333">CUBE_NAME</span></span><br />
<span data-ttu-id="fe56a-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="fe56a-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="fe56a-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-341">-1</span><span class="sxs-lookup"><span data-stu-id="fe56a-341">-1</span></span></p></td>
<td><p><span data-ttu-id="fe56a-342">Se utiliza si el proveedor define sus propias consultas de esquema no estándar.</span><span class="sxs-lookup"><span data-stu-id="fe56a-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="fe56a-343">&lt;Específico del proveedor&gt;</span><span class="sxs-lookup"><span data-stu-id="fe56a-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-345">22</span><span class="sxs-lookup"><span data-stu-id="fe56a-345">22</span></span></p></td>
<td><p><span data-ttu-id="fe56a-346">Devuelve los tipos de datos (base) admitidos por el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="fe56a-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="fe56a-347">(Conjunto de filas PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-348">DATA_TYPE</span></span><br />
<span data-ttu-id="fe56a-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="fe56a-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-351">9 </span><span class="sxs-lookup"><span data-stu-id="fe56a-351">9</span></span></p></td>
<td><p><span data-ttu-id="fe56a-352">Devuelve las restricciones referenciales definidas en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-353">(Conjunto de filas REFERENTIAL_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="fe56a-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-358">17 </span><span class="sxs-lookup"><span data-stu-id="fe56a-358">17</span></span></p></td>
<td><p><span data-ttu-id="fe56a-359">Devuelve los esquemas (objetos de base de datos) que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="fe56a-360">(Conjunto de filas SCHEMATA)</span><span class="sxs-lookup"><span data-stu-id="fe56a-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="fe56a-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="fe56a-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="fe56a-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-365">18 </span><span class="sxs-lookup"><span data-stu-id="fe56a-365">18</span></span></p></td>
<td><p><span data-ttu-id="fe56a-366">Devuelve los niveles de conformidad, las opciones y los dialectos admitidos por los datos de procesamiento de la implementación de SQL definidos en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="fe56a-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="fe56a-367">(Conjunto de filas SQL_LANGUAGES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-368">&lt;Ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="fe56a-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-370">19</span><span class="sxs-lookup"><span data-stu-id="fe56a-370">19</span></span></p></td>
<td><p><span data-ttu-id="fe56a-371">Devuelve las estadísticas definidas en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-372">(Conjunto de filas STATISTICS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-377">10  </span><span class="sxs-lookup"><span data-stu-id="fe56a-377">10</span></span></p></td>
<td><p><span data-ttu-id="fe56a-378">Devuelve las restricciones de tabla definidas en el catálogo que pertenecen a un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="fe56a-379">(Conjunto de filas TABLE_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="fe56a-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="fe56a-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-385">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-388">14 </span><span class="sxs-lookup"><span data-stu-id="fe56a-388">14</span></span></p></td>
<td><p><span data-ttu-id="fe56a-389">Devuelve los privilegios sobre tablas que se definen en el catálogo y que están disponibles para (o los concede) un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="fe56a-390">(Conjunto de filas TABLE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-393">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-394">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="fe56a-394">GRANTOR</span></span><br />
<span data-ttu-id="fe56a-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="fe56a-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-397">20</span><span class="sxs-lookup"><span data-stu-id="fe56a-397">20</span></span></p></td>
<td><p><span data-ttu-id="fe56a-398">Devuelve las tablas (incluidas las vistas) definidas en el catálogo a las que puede tener acceso un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="fe56a-399">(Conjunto de filas TABLES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-402">TABLE_NAME</span></span><br />
<span data-ttu-id="fe56a-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-405"> 21</span><span class="sxs-lookup"><span data-stu-id="fe56a-405">21</span></span></p></td>
<td><p><span data-ttu-id="fe56a-406">Devuelve las conversiones de caracteres que se definen en el catálogo y a las que puede tener acceso un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="fe56a-407">(Conjunto de filas de TRANSLATIONS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="fe56a-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-412">39</span><span class="sxs-lookup"><span data-stu-id="fe56a-412">39</span></span></p></td>
<td><p><span data-ttu-id="fe56a-413">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fe56a-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-415">15 </span><span class="sxs-lookup"><span data-stu-id="fe56a-415">15</span></span></p></td>
<td><p><span data-ttu-id="fe56a-416">Devuelve los privilegios de uso sobre objetos definidos en el catálogo que están disponibles para (o los concede) un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="fe56a-417">(Conjunto de filas USAGE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="fe56a-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="fe56a-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="fe56a-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="fe56a-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="fe56a-422">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="fe56a-422">GRANTOR</span></span><br />
<span data-ttu-id="fe56a-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="fe56a-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-425">24</span><span class="sxs-lookup"><span data-stu-id="fe56a-425">24</span></span></p></td>
<td><p><span data-ttu-id="fe56a-426">Devuelve las columnas sobre las que las tablas vistas, definidas en el catálogo y que pertenecen a un usuario determinado, son dependientes.</span><span class="sxs-lookup"><span data-stu-id="fe56a-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="fe56a-427">(Conjunto de filas VIEW_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="fe56a-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="fe56a-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-432">23</span><span class="sxs-lookup"><span data-stu-id="fe56a-432">23</span></span></p></td>
<td><p><span data-ttu-id="fe56a-433">Devuelve las vistas definidas en el catálogo a las que puede tener acceso un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="fe56a-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="fe56a-434">(Conjunto de filas VIEWS)</span><span class="sxs-lookup"><span data-stu-id="fe56a-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="fe56a-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="fe56a-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="fe56a-439">25</span><span class="sxs-lookup"><span data-stu-id="fe56a-439">25</span></span></p></td>
<td><p><span data-ttu-id="fe56a-440">Devuelve las tablas sobre las que las tablas vistas, definidas en el catálogo y que pertenecen a un usuario determinado, son dependientes.</span><span class="sxs-lookup"><span data-stu-id="fe56a-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="fe56a-441">(Conjunto de filas VIEW_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="fe56a-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="fe56a-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="fe56a-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="fe56a-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="fe56a-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="fe56a-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="fe56a-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fe56a-445">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="fe56a-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="fe56a-446">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fe56a-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe56a-447">Constante</span><span class="sxs-lookup"><span data-stu-id="fe56a-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="fe56a-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="fe56a-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="fe56a-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="fe56a-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="fe56a-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="fe56a-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="fe56a-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe56a-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe56a-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe56a-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="fe56a-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="fe56a-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="fe56a-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="fe56a-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="fe56a-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="fe56a-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="fe56a-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe56a-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="fe56a-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="fe56a-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="fe56a-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="fe56a-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="fe56a-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe56a-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="fe56a-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fe56a-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="fe56a-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="fe56a-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="fe56a-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="fe56a-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="fe56a-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="fe56a-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="fe56a-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="fe56a-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="fe56a-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="fe56a-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="fe56a-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="fe56a-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe56a-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe56a-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="fe56a-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe56a-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="fe56a-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

