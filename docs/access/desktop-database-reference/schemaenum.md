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
# <a name="schemaenum"></a>SchemaEnum

**Se aplica a**: Access 2013, Office 2013

Especifica el tipo de objeto **Recordset** de esquema recuperado por el método [OpenSchema](openschema-method-ado.md).

## <a name="remarks"></a>Observaciones

Información adicional acerca de la función y las columnas que se devuelven para cada constante ADO puede encontrarse en los temas del apéndice B de la *Referencia para programadores de OLE DB*. El nombre de cada tema aparece entre paréntesis en la sección Descripción de la tabla siguiente.

Encontrará información adicional acerca de la función y las columnas que se devuelven para cada constante ADO MD en los temas del capítulo 23 de la documentación de *OLE DB para OLAP* . El nombre de cada tema se enumeran entre paréntesis y marcado con un asterisco (\*) en la columna Descripción de la tabla siguiente.

Convierta los tipos de datos de columnas de la documentación de OLE DB a tipo de datos ADO consultando la columna Descripción del tema [DataTypeEnum](datatypeenum.md) de ADO. Por ejemplo, un tipo de datos OLE DB de **DBTYPE\_WSTR** es equivalente a un tipo de datos ADO de **adWChar**.

ADO genera resultados con el aspecto del esquema para las constantes **adSchemaDBInfoKeywords** y **adSchemaDBInfoLiterals**. ADO crea un **objeto Recordset**y, a continuación, rellena cada fila con los valores devueltos respectivamente por los métodos **GetKeywords** e **IDBInfo:: GetLiteralInfo** . Obtener información adicional acerca de estos métodos puede encontrarse en la sección IDBInfo de la *referencia del programador de OLE DB*.

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
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
<th><p>Columnas de restricción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adSchemaAsserts</strong></p></td>
<td><p>0</p></td>
<td><p>Devuelve las aserciones definidas en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas ASSERTIONS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>1</p></td>
<td><p>Devuelve los atributos físicos asociados con catálogos accesibles del sistema de administración de bases de datos (DBMS).
 (Conjunto de filas CATALOGS)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>2</p></td>
<td><p>Devuelve los conjuntos de caracteres definidos en el catálogo a los que puede tener acceso un usuario determinado.
 (Conjunto de filas CHARACTER_SETS)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCheckConstraints</strong></p></td>
<td><p>5</p></td>
<td><p>Devuelve las restricciones de comprobación definidas en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas CHECK_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>3</p></td>
<td><p>Devuelve las intercalaciones de caracteres definidas en el catálogo a las que puede tener acceso un usuario determinado.
 (Conjunto de filas COLLATIONS)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>13</p></td>
<td><p>Devuelve los privilegios sobre columnas de tablas que se definen en el catálogo y que están disponibles para (o los concede) un usuario determinado.
 (Conjunto de filas COLUMN_PRIVILEGES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
NOMBRECOLUMNA<br />
CONCEDERO<br />
RECEPTOR DE PERMISOS</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>4</p></td>
<td><p>Devuelve las columnas de tablas (incluidas las vistas) definidas en el catálogo a las que puede tener acceso un usuario determinado.
 (Conjunto de filas COLUMNS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
NOMBRECOLUMNA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>11</p></td>
<td><p>Devuelve las columnas definidas en el catálogo que dependen de un dominio definido en el catálogo y pertenecen a un usuario determinado.
 (Conjunto de filas COLUMN_DOMAIN_USAGE)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
NOMBREDEDOMINIO<br />
NOMBRECOLUMNA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>6</p></td>
<td><p>Devuelve las columnas utilizadas por restricciones referenciales, restricciones de exclusividad, restricciones de comprobación y aserciones definidas en el catálogo y que son propiedad de un usuario determinado.
 (Conjunto de filas CONSTRAINT_COLUMN_USAGE)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
NOMBRECOLUMNA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>7</p></td>
<td><p>Devuelve las tablas utilizadas por restricciones referenciales, restricciones de exclusividad, restricciones de comprobación y aserciones definidas en el catálogo y que son propiedad de un usuario determinado.
 (Conjunto de filas CONSTRAINT_TABLE_USAGE)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>Devuelve información acerca de los cubos disponibles en un esquema (o en el catálogo, si el proveedor no admite esquemas).
 (Conjunto de filas CUBE*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDBInfoKeywords</strong></p></td>
<td><p>30</p></td>
<td><p>Devuelve una lista de palabras clave específicas del proveedor.
 (IDBInfo::GetKeywords *)</p></td>
<td><p>&lt;Ninguno&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaDBInfoLiterals</strong></p></td>
<td><p>31</p></td>
<td><p>Devuelve una lista de los literales específicos del proveedor utilizados en comandos de texto.
 (IDBInfo::GetLiteralInfo *)</p></td>
<td><p>&lt;Ninguno&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDimensions</strong></p></td>
<td><p>33</p></td>
<td><p>Devuelve información acerca de las dimensiones de un cubo dado. Tiene una fila para cada dimensión. (Conjunto de filas DIMENSIONS *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>27</p></td>
<td><p>Devuelve las columnas de clave externa definidas por un usuario determinado en el catálogo.
 (Conjunto de filas FOREIGN_KEYS)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaHierarchies</strong></p></td>
<td><p>34</p></td>
<td><p>Devuelve información acerca de las jerarquías disponibles en una dimensión.
 (Conjunto de filas HIERARCHIES *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaIndexes</strong></p></td>
<td><p>12</p></td>
<td><p>Devuelve los índices definidos en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas INDEXES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBREÍNDICE<br />
TIPO DE<br />
NOMBRETABLA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaKeyColumnUsage</strong></p></td>
<td><p>8</p></td>
<td><p>Devuelve las columnas definidas en el catálogo restringidas por un usuario determinado como claves.
 (Conjunto de filas KEY_COLUMN_USAGE)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
NOMBRECOLUMNA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaLevels</strong></p></td>
<td><p>35</p></td>
<td><p>Devuelve información acerca de los niveles disponibles en una dimensión.
 (Conjunto de filas LEVELS *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaMeasures</strong></p></td>
<td><p>36</p></td>
<td><p>Devuelve información acerca de las medidas disponibles.
 (Conjunto de filas MEASURES *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>Devuelve información acerca de los miembros disponibles.
 (Conjunto de filas MEMBERS *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
LEVEL_NUMBER<br />
MEMBER_NAME<br />
MEMBER_UNIQUE_NAME<br />
MEMBER_CAPTION<br />
MEMBER_TYPE<br />
Operador de árbol (para obtener más información, vea OLE DB para la documentación de OLAP).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>28</p></td>
<td><p>Devuelve las columnas de clave principal definidas por un usuario determinado en el catálogo.
 (Conjunto de filas PRIMARY_KEYS)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>29</p></td>
<td><p>Devuelve información acerca de las columnas de conjuntos de filas devueltos por procedimientos.
 (Conjunto de filas PROCEDURE_COLUMNS)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
NOMBRECOLUMNA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>26</p></td>
<td><p>Devuelve información acerca de los parámetros y códigos de retorno de procedimientos.
 (Conjunto de filas PROCEDURE_PARAMETERS)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PARAMETER_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedures</strong></p></td>
<td><p>16</p></td>
<td><p>Devuelve los procedimientos definidos en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas PROCEDURES)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProperties</strong></p></td>
<td><p>37</p></td>
<td><p>Devuelve información acerca de las propiedades disponibles para cada nivel de la dimensión.
 (Conjunto de filas PROPERTIES)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
MEMBER_UNIQUE_NAME<br />
PROPERTY_TYPE<br />
PROPERTY_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>Se utiliza si el proveedor define sus propias consultas de esquema no estándar.</p></td>
<td><p>&lt;Específico del proveedor&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProviderTypes</strong></p></td>
<td><p>22</p></td>
<td><p>Devuelve los tipos de datos (base) admitidos por el proveedor de datos.
 (Conjunto de filas PROVIDER_TYPES)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdSchemaReferentialConstraints</strong></p></td>
<td><p>9</p></td>
<td><p>Devuelve las restricciones referenciales definidas en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas REFERENTIAL_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>17</p></td>
<td><p>Devuelve los esquemas (objetos de base de datos) que pertenecen a un usuario determinado.
 (Conjunto de filas SCHEMATA)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>18</p></td>
<td><p>Devuelve los niveles de conformidad, las opciones y los dialectos admitidos por los datos de procesamiento de la implementación de SQL definidos en el catálogo.
 (Conjunto de filas SQL_LANGUAGES)</p></td>
<td><p>&lt;Ninguno&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaStatistics</strong></p></td>
<td><p>19</p></td>
<td><p>Devuelve las estadísticas definidas en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas STATISTICS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>10</p></td>
<td><p>Devuelve las restricciones de tabla definidas en el catálogo que pertenecen a un usuario determinado.
 (Conjunto de filas TABLE_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTablePrivileges</strong></p></td>
<td><p>14</p></td>
<td><p>Devuelve los privilegios sobre tablas que se definen en el catálogo y que están disponibles para (o los concede) un usuario determinado.
 (Conjunto de filas TABLE_PRIVILEGES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
CONCEDERO<br />
RECEPTOR DE PERMISOS</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTables</strong></p></td>
<td><p>20</p></td>
<td><p>Devuelve las tablas (incluidas las vistas) definidas en el catálogo a las que puede tener acceso un usuario determinado.
 (Conjunto de filas TABLES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTranslations</strong></p></td>
<td><p>21</p></td>
<td><p>Devuelve las conversiones de caracteres que se definen en el catálogo y a las que puede tener acceso un usuario determinado.
 (Conjunto de filas de TRANSLATIONS)</p></td>
<td><p>TRANSLATION_CATALOG<br />
TRANSLATION_SCHEMA<br />
TRANSLATION_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTrustees</strong></p></td>
<td><p>39</p></td>
<td><p>Reservado para uso futuro.</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaUsagePrivileges</strong></p></td>
<td><p>15</p></td>
<td><p>Devuelve los privilegios de uso sobre objetos definidos en el catálogo que están disponibles para (o los concede) un usuario determinado.
 (Conjunto de filas USAGE_PRIVILEGES)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
OBJECT_TYPE<br />
CONCEDERO<br />
RECEPTOR DE PERMISOS</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewColumnUsage</strong></p></td>
<td><p>24</p></td>
<td><p>Devuelve las columnas sobre las que las tablas vistas, definidas en el catálogo y que pertenecen a un usuario determinado, son dependientes.
 (Conjunto de filas VIEW_COLUMN_USAGE)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
NOMBREVISTA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaViews</strong></p></td>
<td><p>23</p></td>
<td><p>Devuelve las vistas definidas en el catálogo a las que puede tener acceso un usuario determinado.
 (Conjunto de filas VIEWS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
NOMBRETABLA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewTableUsage</strong></p></td>
<td><p>25</p></td>
<td><p>Devuelve las tablas sobre las que las tablas vistas, definidas en el catálogo y que pertenecen a un usuario determinado, son dependientes.
 (Conjunto de filas VIEW_TABLE_USAGE)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
NOMBREVISTA</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Paquete: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Schema.ASSERTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CATALOGS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CHARACTERSETS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CHECKCONSTRAINTS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLLATIONS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNSDOMAINUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CUBES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DIMENSIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.HIERARCHIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.INDEXES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.KEYCOLUMNUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.LEVELS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.MEASURES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.MEMBERS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PRIMARYKEYS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROCEDUREPARAMETERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROVIDERSPECIFIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROVIDERTYPES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.SQLLANGUAGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.STATISTICS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TABLEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TRANSLATIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TRUSTEES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.USAGEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.VIEWS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWTABLEUSAGE</p></td>
</tr>
</tbody>
</table>

