---
title: SchemaEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718829"
---
# <a name="schemaenum"></a><span data-ttu-id="8970f-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="8970f-102">SchemaEnum</span></span>

<span data-ttu-id="8970f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8970f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8970f-104">Especifica el tipo de objeto **Recordset** de esquema recuperado por el método [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8970f-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="8970f-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8970f-105">Remarks</span></span>

<span data-ttu-id="8970f-106">Información adicional acerca de la función y las columnas que se devuelven para cada constante ADO puede encontrarse en los temas del apéndice B de la *Referencia para programadores de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="8970f-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="8970f-107">El nombre de cada tema aparece entre paréntesis en la sección Descripción de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8970f-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="8970f-108">Encontrará información adicional acerca de la función y las columnas que se devuelven para cada constante ADO MD en los temas del capítulo 23 de la documentación de *OLE DB para OLAP* .</span><span class="sxs-lookup"><span data-stu-id="8970f-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="8970f-109">El nombre de cada tema se enumeran entre paréntesis y marcado con un asterisco (\*) en la columna Descripción de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8970f-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="8970f-110">Convierta los tipos de datos de columnas de la documentación de OLE DB a tipo de datos ADO consultando la columna Descripción del tema [DataTypeEnum](datatypeenum.md) de ADO.</span><span class="sxs-lookup"><span data-stu-id="8970f-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="8970f-111">Por ejemplo, un tipo de datos OLE DB de **DBTYPE\_WSTR** es equivalente a un tipo de datos ADO de **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="8970f-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="8970f-112">ADO genera resultados con el aspecto del esquema para las constantes **adSchemaDBInfoKeywords** y **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="8970f-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="8970f-113">ADO crea un **objeto Recordset**y, a continuación, rellena cada fila con los valores devueltos respectivamente por los métodos **GetKeywords** e **IDBInfo:: GetLiteralInfo** .</span><span class="sxs-lookup"><span data-stu-id="8970f-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="8970f-114">Obtener información adicional acerca de estos métodos puede encontrarse en la sección IDBInfo de la *referencia del programador de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="8970f-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="8970f-115">Constante</span><span class="sxs-lookup"><span data-stu-id="8970f-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="8970f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8970f-116">Value</span></span></p></th>
<th><p><span data-ttu-id="8970f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8970f-117">Description</span></span></p></th>
<th><p><span data-ttu-id="8970f-118">Columnas de restricción</span><span class="sxs-lookup"><span data-stu-id="8970f-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8970f-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-120">0</span><span class="sxs-lookup"><span data-stu-id="8970f-120">0</span></span></p></td>
<td><p><span data-ttu-id="8970f-121">Devuelve las aserciones definidas en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-122">(Conjunto de filas ASSERTIONS)</span><span class="sxs-lookup"><span data-stu-id="8970f-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="8970f-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="8970f-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-127">1</span><span class="sxs-lookup"><span data-stu-id="8970f-127">1</span></span></p></td>
<td><p><span data-ttu-id="8970f-128">Devuelve los atributos físicos asociados con catálogos accesibles del sistema de administración de bases de datos (DBMS).
</span><span class="sxs-lookup"><span data-stu-id="8970f-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="8970f-129">(Conjunto de filas CATALOGS)</span><span class="sxs-lookup"><span data-stu-id="8970f-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-132">2</span><span class="sxs-lookup"><span data-stu-id="8970f-132">2</span></span></p></td>
<td><p><span data-ttu-id="8970f-133">Devuelve los conjuntos de caracteres definidos en el catálogo a los que puede tener acceso un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="8970f-134">(Conjunto de filas CHARACTER_SETS)</span><span class="sxs-lookup"><span data-stu-id="8970f-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="8970f-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="8970f-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-139">5</span><span class="sxs-lookup"><span data-stu-id="8970f-139">5</span></span></p></td>
<td><p><span data-ttu-id="8970f-140">Devuelve las restricciones de comprobación definidas en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-141">(Conjunto de filas CHECK_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="8970f-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="8970f-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="8970f-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-146">3</span><span class="sxs-lookup"><span data-stu-id="8970f-146">3</span></span></p></td>
<td><p><span data-ttu-id="8970f-147">Devuelve las intercalaciones de caracteres definidas en el catálogo a las que puede tener acceso un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="8970f-148">(Conjunto de filas COLLATIONS)</span><span class="sxs-lookup"><span data-stu-id="8970f-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="8970f-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="8970f-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-153">13</span><span class="sxs-lookup"><span data-stu-id="8970f-153">13</span></span></p></td>
<td><p><span data-ttu-id="8970f-154">Devuelve los privilegios sobre columnas de tablas que se definen en el catálogo y que están disponibles para (o los concede) un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="8970f-155">(Conjunto de filas COLUMN_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="8970f-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-158">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-158">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-159">NOMBRECOLUMNA</span><span class="sxs-lookup"><span data-stu-id="8970f-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="8970f-160">CONCEDERO</span><span class="sxs-lookup"><span data-stu-id="8970f-160">GRANTOR</span></span><br />
<span data-ttu-id="8970f-161">RECEPTOR DE PERMISOS</span><span class="sxs-lookup"><span data-stu-id="8970f-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-163">4</span><span class="sxs-lookup"><span data-stu-id="8970f-163">4</span></span></p></td>
<td><p><span data-ttu-id="8970f-164">Devuelve las columnas de tablas (incluidas las vistas) definidas en el catálogo a las que puede tener acceso un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="8970f-165">(Conjunto de filas COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="8970f-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-168">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-168">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-169">NOMBRECOLUMNA</span><span class="sxs-lookup"><span data-stu-id="8970f-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-171">11</span><span class="sxs-lookup"><span data-stu-id="8970f-171">11</span></span></p></td>
<td><p><span data-ttu-id="8970f-172">Devuelve las columnas definidas en el catálogo que dependen de un dominio definido en el catálogo y pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="8970f-173">(Conjunto de filas COLUMN_DOMAIN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="8970f-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="8970f-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="8970f-176">NOMBREDEDOMINIO</span><span class="sxs-lookup"><span data-stu-id="8970f-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="8970f-177">NOMBRECOLUMNA</span><span class="sxs-lookup"><span data-stu-id="8970f-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-179">6</span><span class="sxs-lookup"><span data-stu-id="8970f-179">6</span></span></p></td>
<td><p><span data-ttu-id="8970f-180">Devuelve las columnas utilizadas por restricciones referenciales, restricciones de exclusividad, restricciones de comprobación y aserciones definidas en el catálogo y que son propiedad de un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="8970f-181">(Conjunto de filas CONSTRAINT_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="8970f-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-184">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-184">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-185">NOMBRECOLUMNA</span><span class="sxs-lookup"><span data-stu-id="8970f-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-187">7</span><span class="sxs-lookup"><span data-stu-id="8970f-187">7</span></span></p></td>
<td><p><span data-ttu-id="8970f-188">Devuelve las tablas utilizadas por restricciones referenciales, restricciones de exclusividad, restricciones de comprobación y aserciones definidas en el catálogo y que son propiedad de un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="8970f-189">(Conjunto de filas CONSTRAINT_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="8970f-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-192">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-194">32</span><span class="sxs-lookup"><span data-stu-id="8970f-194">32</span></span></p></td>
<td><p><span data-ttu-id="8970f-195">Devuelve información acerca de los cubos disponibles en un esquema (o en el catálogo, si el proveedor no admite esquemas).
</span><span class="sxs-lookup"><span data-stu-id="8970f-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="8970f-196">(Conjunto de filas CUBE\*)</span><span class="sxs-lookup"><span data-stu-id="8970f-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-201">30</span><span class="sxs-lookup"><span data-stu-id="8970f-201">30</span></span></p></td>
<td><p><span data-ttu-id="8970f-202">Devuelve una lista de palabras clave específicas del proveedor.
</span><span class="sxs-lookup"><span data-stu-id="8970f-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="8970f-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-204">&lt;Ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="8970f-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-206">31</span><span class="sxs-lookup"><span data-stu-id="8970f-206">31</span></span></p></td>
<td><p><span data-ttu-id="8970f-207">Devuelve una lista de los literales específicos del proveedor utilizados en comandos de texto.
</span><span class="sxs-lookup"><span data-stu-id="8970f-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="8970f-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-209">&lt;Ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="8970f-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-211">33</span><span class="sxs-lookup"><span data-stu-id="8970f-211">33</span></span></p></td>
<td><p><span data-ttu-id="8970f-212">Devuelve información acerca de las dimensiones de un cubo dado.</span><span class="sxs-lookup"><span data-stu-id="8970f-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="8970f-213">Tiene una fila para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="8970f-213">It has one row for each dimension.</span></span> <span data-ttu-id="8970f-214">(Conjunto de filas DIMENSIONS \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-217">CUBE_NAME</span></span><br />
<span data-ttu-id="8970f-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="8970f-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-221">27</span><span class="sxs-lookup"><span data-stu-id="8970f-221">27</span></span></p></td>
<td><p><span data-ttu-id="8970f-222">Devuelve las columnas de clave externa definidas por un usuario determinado en el catálogo.
</span><span class="sxs-lookup"><span data-stu-id="8970f-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="8970f-223">(Conjunto de filas FOREIGN_KEYS)</span><span class="sxs-lookup"><span data-stu-id="8970f-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-231">34</span><span class="sxs-lookup"><span data-stu-id="8970f-231">34</span></span></p></td>
<td><p><span data-ttu-id="8970f-232">Devuelve información acerca de las jerarquías disponibles en una dimensión.
</span><span class="sxs-lookup"><span data-stu-id="8970f-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="8970f-233">(Conjunto de filas HIERARCHIES \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-236">CUBE_NAME</span></span><br />
<span data-ttu-id="8970f-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="8970f-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-241">12</span><span class="sxs-lookup"><span data-stu-id="8970f-241">12</span></span></p></td>
<td><p><span data-ttu-id="8970f-242">Devuelve los índices definidos en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-243">(Conjunto de filas INDEXES)</span><span class="sxs-lookup"><span data-stu-id="8970f-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-246">NOMBREÍNDICE</span><span class="sxs-lookup"><span data-stu-id="8970f-246">INDEX_NAME</span></span><br />
<span data-ttu-id="8970f-247">TIPO DE</span><span class="sxs-lookup"><span data-stu-id="8970f-247">TYPE</span></span><br />
<span data-ttu-id="8970f-248">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-250">8</span><span class="sxs-lookup"><span data-stu-id="8970f-250">8</span></span></p></td>
<td><p><span data-ttu-id="8970f-251">Devuelve las columnas definidas en el catálogo restringidas por un usuario determinado como claves.
</span><span class="sxs-lookup"><span data-stu-id="8970f-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="8970f-252">(Conjunto de filas KEY_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="8970f-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="8970f-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="8970f-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="8970f-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-258">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-258">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-259">NOMBRECOLUMNA</span><span class="sxs-lookup"><span data-stu-id="8970f-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-261">35</span><span class="sxs-lookup"><span data-stu-id="8970f-261">35</span></span></p></td>
<td><p><span data-ttu-id="8970f-262">Devuelve información acerca de los niveles disponibles en una dimensión.
</span><span class="sxs-lookup"><span data-stu-id="8970f-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="8970f-263">(Conjunto de filas LEVELS \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-266">CUBE_NAME</span></span><br />
<span data-ttu-id="8970f-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="8970f-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-272">36</span><span class="sxs-lookup"><span data-stu-id="8970f-272">36</span></span></p></td>
<td><p><span data-ttu-id="8970f-273">Devuelve información acerca de las medidas disponibles.
</span><span class="sxs-lookup"><span data-stu-id="8970f-273">Returns information about the available measures.</span></span> <span data-ttu-id="8970f-274">(Conjunto de filas MEASURES \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-277">CUBE_NAME</span></span><br />
<span data-ttu-id="8970f-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="8970f-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-281">38</span><span class="sxs-lookup"><span data-stu-id="8970f-281">38</span></span></p></td>
<td><p><span data-ttu-id="8970f-282">Devuelve información acerca de los miembros disponibles.
</span><span class="sxs-lookup"><span data-stu-id="8970f-282">Returns information about the available members.</span></span> <span data-ttu-id="8970f-283">(Conjunto de filas MEMBERS \*)</span><span class="sxs-lookup"><span data-stu-id="8970f-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-286">CUBE_NAME</span></span><br />
<span data-ttu-id="8970f-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="8970f-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="8970f-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="8970f-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="8970f-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="8970f-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="8970f-295">Operador de árbol (para obtener más información, vea OLE DB para la documentación de OLAP).</span><span class="sxs-lookup"><span data-stu-id="8970f-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-297">28</span><span class="sxs-lookup"><span data-stu-id="8970f-297">28</span></span></p></td>
<td><p><span data-ttu-id="8970f-298">Devuelve las columnas de clave principal definidas por un usuario determinado en el catálogo.
</span><span class="sxs-lookup"><span data-stu-id="8970f-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="8970f-299">(Conjunto de filas PRIMARY_KEYS)</span><span class="sxs-lookup"><span data-stu-id="8970f-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-304">29</span><span class="sxs-lookup"><span data-stu-id="8970f-304">29</span></span></p></td>
<td><p><span data-ttu-id="8970f-305">Devuelve información acerca de las columnas de conjuntos de filas devueltos por procedimientos.
</span><span class="sxs-lookup"><span data-stu-id="8970f-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="8970f-306">(Conjunto de filas PROCEDURE_COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="8970f-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="8970f-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="8970f-310">NOMBRECOLUMNA</span><span class="sxs-lookup"><span data-stu-id="8970f-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-312">26</span><span class="sxs-lookup"><span data-stu-id="8970f-312">26</span></span></p></td>
<td><p><span data-ttu-id="8970f-313">Devuelve información acerca de los parámetros y códigos de retorno de procedimientos.
</span><span class="sxs-lookup"><span data-stu-id="8970f-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="8970f-314">(Conjunto de filas PROCEDURE_PARAMETERS)</span><span class="sxs-lookup"><span data-stu-id="8970f-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="8970f-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="8970f-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-320">16</span><span class="sxs-lookup"><span data-stu-id="8970f-320">16</span></span></p></td>
<td><p><span data-ttu-id="8970f-321">Devuelve los procedimientos definidos en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-322">(Conjunto de filas PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="8970f-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="8970f-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="8970f-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-328">37</span><span class="sxs-lookup"><span data-stu-id="8970f-328">37</span></span></p></td>
<td><p><span data-ttu-id="8970f-329">Devuelve información acerca de las propiedades disponibles para cada nivel de la dimensión.
</span><span class="sxs-lookup"><span data-stu-id="8970f-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="8970f-330">(Conjunto de filas PROPERTIES)</span><span class="sxs-lookup"><span data-stu-id="8970f-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="8970f-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-333">CUBE_NAME</span></span><br />
<span data-ttu-id="8970f-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="8970f-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="8970f-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-341">-1</span><span class="sxs-lookup"><span data-stu-id="8970f-341">-1</span></span></p></td>
<td><p><span data-ttu-id="8970f-342">Se utiliza si el proveedor define sus propias consultas de esquema no estándar.</span><span class="sxs-lookup"><span data-stu-id="8970f-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="8970f-343">&lt;Específico del proveedor&gt;</span><span class="sxs-lookup"><span data-stu-id="8970f-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-345">22</span><span class="sxs-lookup"><span data-stu-id="8970f-345">22</span></span></p></td>
<td><p><span data-ttu-id="8970f-346">Devuelve los tipos de datos (base) admitidos por el proveedor de datos.
</span><span class="sxs-lookup"><span data-stu-id="8970f-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="8970f-347">(Conjunto de filas PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="8970f-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-348">DATA_TYPE</span></span><br />
<span data-ttu-id="8970f-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="8970f-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-351">9</span><span class="sxs-lookup"><span data-stu-id="8970f-351">9</span></span></p></td>
<td><p><span data-ttu-id="8970f-352">Devuelve las restricciones referenciales definidas en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-353">(Conjunto de filas REFERENTIAL_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="8970f-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="8970f-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="8970f-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-358">17</span><span class="sxs-lookup"><span data-stu-id="8970f-358">17</span></span></p></td>
<td><p><span data-ttu-id="8970f-359">Devuelve los esquemas (objetos de base de datos) que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="8970f-360">(Conjunto de filas SCHEMATA)</span><span class="sxs-lookup"><span data-stu-id="8970f-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="8970f-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="8970f-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="8970f-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-365">18</span><span class="sxs-lookup"><span data-stu-id="8970f-365">18</span></span></p></td>
<td><p><span data-ttu-id="8970f-366">Devuelve los niveles de conformidad, las opciones y los dialectos admitidos por los datos de procesamiento de la implementación de SQL definidos en el catálogo.
</span><span class="sxs-lookup"><span data-stu-id="8970f-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="8970f-367">(Conjunto de filas SQL_LANGUAGES)</span><span class="sxs-lookup"><span data-stu-id="8970f-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-368">&lt;Ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="8970f-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-370">19</span><span class="sxs-lookup"><span data-stu-id="8970f-370">19</span></span></p></td>
<td><p><span data-ttu-id="8970f-371">Devuelve las estadísticas definidas en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-372">(Conjunto de filas STATISTICS)</span><span class="sxs-lookup"><span data-stu-id="8970f-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-375">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-377">10</span><span class="sxs-lookup"><span data-stu-id="8970f-377">10</span></span></p></td>
<td><p><span data-ttu-id="8970f-378">Devuelve las restricciones de tabla definidas en el catálogo que pertenecen a un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="8970f-379">(Conjunto de filas TABLE_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="8970f-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="8970f-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="8970f-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="8970f-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-385">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-385">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-388">14</span><span class="sxs-lookup"><span data-stu-id="8970f-388">14</span></span></p></td>
<td><p><span data-ttu-id="8970f-389">Devuelve los privilegios sobre tablas que se definen en el catálogo y que están disponibles para (o los concede) un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="8970f-390">(Conjunto de filas TABLE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="8970f-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-393">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-393">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-394">CONCEDERO</span><span class="sxs-lookup"><span data-stu-id="8970f-394">GRANTOR</span></span><br />
<span data-ttu-id="8970f-395">RECEPTOR DE PERMISOS</span><span class="sxs-lookup"><span data-stu-id="8970f-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-397">20</span><span class="sxs-lookup"><span data-stu-id="8970f-397">20</span></span></p></td>
<td><p><span data-ttu-id="8970f-398">Devuelve las tablas (incluidas las vistas) definidas en el catálogo a las que puede tener acceso un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="8970f-399">(Conjunto de filas TABLES)</span><span class="sxs-lookup"><span data-stu-id="8970f-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-402">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-402">TABLE_NAME</span></span><br />
<span data-ttu-id="8970f-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-405">21</span><span class="sxs-lookup"><span data-stu-id="8970f-405">21</span></span></p></td>
<td><p><span data-ttu-id="8970f-406">Devuelve las conversiones de caracteres que se definen en el catálogo y a las que puede tener acceso un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="8970f-407">(Conjunto de filas de TRANSLATIONS)</span><span class="sxs-lookup"><span data-stu-id="8970f-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="8970f-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="8970f-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-412">39</span><span class="sxs-lookup"><span data-stu-id="8970f-412">39</span></span></p></td>
<td><p><span data-ttu-id="8970f-413">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8970f-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-415">15</span><span class="sxs-lookup"><span data-stu-id="8970f-415">15</span></span></p></td>
<td><p><span data-ttu-id="8970f-416">Devuelve los privilegios de uso sobre objetos definidos en el catálogo que están disponibles para (o los concede) un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="8970f-417">(Conjunto de filas USAGE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="8970f-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="8970f-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="8970f-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="8970f-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="8970f-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="8970f-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="8970f-422">CONCEDERO</span><span class="sxs-lookup"><span data-stu-id="8970f-422">GRANTOR</span></span><br />
<span data-ttu-id="8970f-423">RECEPTOR DE PERMISOS</span><span class="sxs-lookup"><span data-stu-id="8970f-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-425">24</span><span class="sxs-lookup"><span data-stu-id="8970f-425">24</span></span></p></td>
<td><p><span data-ttu-id="8970f-426">Devuelve las columnas sobre las que las tablas vistas, definidas en el catálogo y que pertenecen a un usuario determinado, son dependientes.
</span><span class="sxs-lookup"><span data-stu-id="8970f-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="8970f-427">(Conjunto de filas VIEW_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="8970f-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="8970f-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="8970f-430">NOMBREVISTA</span><span class="sxs-lookup"><span data-stu-id="8970f-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-432">23</span><span class="sxs-lookup"><span data-stu-id="8970f-432">23</span></span></p></td>
<td><p><span data-ttu-id="8970f-433">Devuelve las vistas definidas en el catálogo a las que puede tener acceso un usuario determinado.
</span><span class="sxs-lookup"><span data-stu-id="8970f-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="8970f-434">(Conjunto de filas VIEWS)</span><span class="sxs-lookup"><span data-stu-id="8970f-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="8970f-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="8970f-437">NOMBRETABLA</span><span class="sxs-lookup"><span data-stu-id="8970f-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="8970f-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="8970f-439">25</span><span class="sxs-lookup"><span data-stu-id="8970f-439">25</span></span></p></td>
<td><p><span data-ttu-id="8970f-440">Devuelve las tablas sobre las que las tablas vistas, definidas en el catálogo y que pertenecen a un usuario determinado, son dependientes.
</span><span class="sxs-lookup"><span data-stu-id="8970f-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="8970f-441">(Conjunto de filas VIEW_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="8970f-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="8970f-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="8970f-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="8970f-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="8970f-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="8970f-444">NOMBREVISTA</span><span class="sxs-lookup"><span data-stu-id="8970f-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8970f-445">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8970f-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="8970f-446">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8970f-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8970f-447">Constante</span><span class="sxs-lookup"><span data-stu-id="8970f-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8970f-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="8970f-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="8970f-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="8970f-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="8970f-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="8970f-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="8970f-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="8970f-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="8970f-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="8970f-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="8970f-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="8970f-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="8970f-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="8970f-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="8970f-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="8970f-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="8970f-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="8970f-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="8970f-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="8970f-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="8970f-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="8970f-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="8970f-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="8970f-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8970f-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="8970f-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8970f-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="8970f-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="8970f-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="8970f-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="8970f-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="8970f-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="8970f-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="8970f-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="8970f-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="8970f-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="8970f-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="8970f-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="8970f-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="8970f-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8970f-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="8970f-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8970f-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="8970f-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

