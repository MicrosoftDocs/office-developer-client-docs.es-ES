---
title: Miembros del campo (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 497c0375496310c27c134792e01bd17e5533a452
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922205"
---
# <a name="field-members-dao"></a><span data-ttu-id="31306-102">Miembros del campo (DAO)</span><span class="sxs-lookup"><span data-stu-id="31306-102">Field members (DAO)</span></span>


<span data-ttu-id="31306-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31306-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31306-104">Un objeto Field representa una columna de datos con un tipo de datos común y un conjunto de propiedades común.</span><span class="sxs-lookup"><span data-stu-id="31306-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="31306-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="31306-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31306-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="31306-106">Name</span></span></p></th>
<th><p><span data-ttu-id="31306-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="31306-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31306-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-109">Agrega datos de una expresión de cadena a un objeto <strong><a href="field-object-dao.md">Field</a></strong> de Memo o binario largo en un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="31306-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-111">Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="31306-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-113">Devuelve todo o parte del contenido de un objeto <strong>Memo</strong> o <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="31306-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="31306-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31306-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31306-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="31306-115">Name</span></span></p></th>
<th><p><span data-ttu-id="31306-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="31306-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31306-117"><strong><a href="field-allowzerolength-property-dao.md">Permitir longitud cero</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-118">Establece o devuelve un valor que indica si una cadena de longitud cero (&quot;&quot;) es un valor válido para la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> del objeto <strong><a href="field-object-dao.md">Field</a></strong> con un tipo de datos texto o Memo (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="31306-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p101">Establece o devuelve un valor que indica una o varias características de un objeto <strong><a href="field-object-dao.md">Field</a></strong>. <strong>Long</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31306-p101">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p102">Devuelve un valor que especifica la secuencia del criterio de ordenación en texto para comparación u ordenación de la cadena (sólo para áreas de trabajo de Microsoft Access). <strong>Long</strong> de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="31306-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-126">Devuelve un valor que indica si los datos del campo representado por un objeto <strong><a href="field-object-dao.md">Field</a></strong> se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="31306-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p103">Establece o devuelve el valor predeterminado de un objeto <strong><a href="field-object-dao.md">Field</a></strong>. Para un objeto <strong>Field</strong> que todavía no se ha anexado a la colección <strong><a href="fields-collection-dao.md">Fields</a></strong>, esta propiedad es de lectura y escritura (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="31306-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-130"><strong><a href="field-fieldsize-property-dao.md">TamañoDelCampo</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-131">Devuelve el número de bytes usados en la base de datos (en lugar de en la memoria) de un objeto Memo o Long Binary <strong><a href="field-object-dao.md">Field</a></strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="31306-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-133">Establece o devuelve un valor que especifica el nombre del objeto <strong><a href="field-object-dao.md">Field</a></strong> en una tabla externa que corresponde a un campo en una tabla primaria para una relación (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="31306-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p104">Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</span><span class="sxs-lookup"><span data-stu-id="31306-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p105">Establece o devuelve la posición relativa de un objeto <strong><a href="field-object-dao.md">Field</a></strong> en una colección <strong><a href="fields-collection-dao.md">Fields</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="31306-p105">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection. .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="31306-p106">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="31306-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="31306-144">Devuelve el valor de un <strong>Field</strong> en la base de datos existente cuando comienza la actualización del último lote (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="31306-144">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-145"><strong><a href="field-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-145"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p107">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</span><span class="sxs-lookup"><span data-stu-id="31306-p107">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-148"><strong><a href="field-required-property-dao.md">Obligatorio</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-148"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-149">Establece o devuelve un valor que indica si un objeto <strong><a href="field-object-dao.md">Field</a></strong> requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="31306-149">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-150"><strong><a href="field-fieldsize-property-dao.md">Tamaño</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-150"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-151">Devuelve el número de bytes usados en la base de datos (en lugar de en la memoria) de un objeto Memo o Long Binary <strong><a href="field-object-dao.md">Field</a></strong> en la colección <strong><a href="fields-collection-dao.md">Fields</a></strong> de un objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="31306-151">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p108">Devuelve un valor que indica el nombre del campo que es el origen de los datos correspondientes a un objeto <strong>Field</strong>. <strong>String</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="31306-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p109">Devuelve un valor que indica el nombre de la tabla que es la fuente original de los datos para un objeto <strong>Field</strong>. <strong>String</strong> de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="31306-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-158"><strong><a href="field-type-property-dao.md">Tipo de</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-158"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p110">Establece un valor que indica el tipo operativo o de datos de un objeto. <strong>Integer</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31306-p110">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-162">Establece o devuelve un valor que especifica si el valor de un objeto <strong><a href="field-object-dao.md">Field</a></strong> se valida o no inmediatamente cuando se establece la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> del objeto (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="31306-162">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p111">Establece o devuelve un valor que valida los datos de un campo cuando se cambia o agrega a una tabla (únicamente áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31306-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p112">Establece o devuelve un valor que especifica el texto del mensaje que la aplicación muestra si el valor de un objeto <strong>Field</strong> no cumple la regla de validación especificada por el valor de la propiedad <strong>ValidationRule</strong> (únicamente áreas de trabajo de Microsoft Access). <strong>String</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31306-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31306-169"><strong><a href="field-value-property-dao.md">Valor</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-169"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="31306-p113">Establece o devuelve el valor de un objeto. <strong>Variant</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="31306-p113">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31306-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="31306-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="31306-p114">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="31306-p114">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="31306-175">Devuelve un valor existente en la base de datos que es más actual que la propiedad <strong>OriginalValue</strong> según lo determinado por un conflicto de actualización por lotes (sólo para áreas de trabajo de ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="31306-175">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

