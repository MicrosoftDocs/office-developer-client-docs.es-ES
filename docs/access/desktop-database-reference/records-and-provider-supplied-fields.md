---
title: Registros y campos proporcionados por el proveedor
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ebbfeb303bb575928f09858db5d3a34cf2171ce0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300759"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="8d0bd-102">Registros y campos proporcionados por el proveedor</span><span class="sxs-lookup"><span data-stu-id="8d0bd-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="8d0bd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d0bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d0bd-104">Cuando se abre un objeto [Record](record-object-ado.md), su origen puede ser la actual fila de un objeto [Recordset](recordset-object-ado.md) abierto, una dirección URL absoluta o una dirección URL relativa junto con un objeto [Connection](connection-object-ado.md) abierto.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="8d0bd-105">Si el objeto **Record** se abre desde un objeto **Recordset**, la colección **Fields** del objeto [Record](fields-collection-ado.md) contendrá todos los campos de **Recordset**, además de los campos agregados por el proveedor subyacente.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="8d0bd-p101">El proveedor puede insertar campos adicionales que sirven de características complementarias del objeto **Record**. Como resultado, un objeto **Record** puede tener campos únicos no incluidos en el objeto **Recordset** como conjunto o cualquier objeto **Record** derivado de otra fila del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p101">The provider may insert additional fields that serve as supplementary characteristics of the **Record**. As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="8d0bd-108">Por ejemplo, todas las filas de un **objeto Recordset** derivado de un origen de datos de correo electrónico podrían tener columnas como from, to y Subject.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-108">For example, all rows of a **Recordset** derived from an email data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="8d0bd-109">Un objeto **Record** derivado de ese objeto **Recordset** tendrá los mismos campos.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="8d0bd-110">Sin embargo, el objeto **Record** también puede tener otros campos únicos para el mensaje concreto representado por ese **Record**, como Datos adjuntos y CC (Con copia).</span><span class="sxs-lookup"><span data-stu-id="8d0bd-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="8d0bd-111">Si bien el objeto **Record** y la actual fila del objeto **Recordset** tienen los mismos campos, son diferentes porque los objetos **Record** y **Recordset** tienen métodos y propiedades distintos.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="8d0bd-p103">Un campo que tienen en común **Record** y **Recordset** puede modificarse en cualquiera de los objetos. Sin embargo, el campo no se puede eliminar en el objeto **Record**, aunque el proveedor subyacente permita establecer el campo en null.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p103">A field held in common by the **Record** and **Recordset** can be modified on either object. However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="8d0bd-p104">Tras abrir el objeto **Record**, puede agregar campos mediante programación. También puede eliminar los campos que agregó, pero no puede eliminar campos del objeto **Recordset** original.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p104">After the **Record** is opened, you can programmatically add fields. You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="8d0bd-p105">Asimismo, puede abrir el objeto **Record** directamente desde una dirección URL. En este caso, los campos agregados al objeto **Record** dependen del proveedor subyacente. Actualmente, la mayoría de los proveedores agregan un conjunto de campos que describen la entidad representada por el objeto **Record**. Si la entidad consta de una secuencia de bytes, como un archivo simple, normalmente se puede abrir un objeto [Stream](stream-object-ado.md) desde el objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p105">You may also open the **Record** object directly from a URL. In this case, the fields added to the **Record** depend on the underlying provider. Currently, most providers add a set of fields that describe the entity represented by the **Record**. If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="8d0bd-120">Campos especiales para proveedores de orígenes de documentos</span><span class="sxs-lookup"><span data-stu-id="8d0bd-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="8d0bd-p106">Una clase especial de proveedores, denominados *proveedores de orígenes de documentos*, administra las carpetas y los documentos. Cuando un objeto **Record** representa un documento o un objeto **Recordset** representa una carpeta de documentos, el proveedor de orígenes de documentos rellena esos objetos con un conjunto único de campos que describen las características del documento en lugar del propio documento. Normalmente, un campo contiene una referencia al objeto **Stream** que representa el documento.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p106">A special class of providers, called *document source providers*, manages folders and documents. When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself. Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="8d0bd-124">Estos campos constituyen un objeto **Record** o **Recordset** de recurso y se enumeran para los proveedores específicos que los admiten en [Apéndice A: Proveedores](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="8d0bd-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="8d0bd-p107">Dos constantes indican la colección **Fields** de un objeto **Record** o **Recordset** de recurso para recuperar un par de campos de uso común. La propiedad **Value** del objeto [Field](value-property-ado.md) devuelve el contenido deseado.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p107">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields. The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="8d0bd-p108">El campo al que se obtiene acceso con la constante **adDefaultStream** contiene una secuencia asociada al objeto **Record** o **Recordset**. El proveedor asigna una secuencia predeterminada a un objeto.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p108">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object. The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="8d0bd-129">El campo al que se obtiene acceso con la constante **adRecordURL** contiene la dirección URL absoluta que identifica el documento.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="8d0bd-p109">Un proveedor de orígenes de documentos no admite la colección [Properties](properties-collection-ado.md) de los objetos **Record** y **Field**. El contenido de la colección **Properties** es nulo para dichos objetos.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p109">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects. The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="8d0bd-p110">Un proveedor de orígenes de documentos puede agregar una propiedad específica, como **Datasource Type**, para identificar si es un proveedor de orígenes de documentos. Para obtener más información sobre cómo determinar el tipo de proveedor, vea la documentación de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p110">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider. For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="8d0bd-134">Columnas de conjuntos de registros de recurso</span><span class="sxs-lookup"><span data-stu-id="8d0bd-134">Resource Recordset Columns</span></span>

<span data-ttu-id="8d0bd-135">Un *conjunto de registros de recurso* consta de las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d0bd-136">Nombre de columna</span><span class="sxs-lookup"><span data-stu-id="8d0bd-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="8d0bd-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d0bd-137">Type</span></span></p></th>
<th><p><span data-ttu-id="8d0bd-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d0bd-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p111">Sólo lectura.

Indica la dirección URL del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p111">Read-only. Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p112">Sólo lectura.

Indica la dirección URL absoluta del registro primario.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p112">Read-only. Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p113">Sólo lectura.

Indica la dirección URL absoluta del recurso, que es la concatenación de PARENTNAME y PARSENAME.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p113">Read-only. Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="8d0bd-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="8d0bd-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p114">Es True si el recurso está oculto.

No se devolverá ninguna fila, a menos que el comando que crea el conjunto de filas seleccione explícitamente filas donde el valor de RESOURCE_ISHIDDEN es True.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p114">True if the resource is hidden. No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="8d0bd-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="8d0bd-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p115">Es True si el recurso es de sólo lectura.

Al intentar abrir este recurso con DBBINDFLAG_WRITE, se generará un error con DB_E_READONLY.

Esta propiedad se puede modificar, incluso si el recurso se ha abierto sólo para leerlo.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p115">True if the resource is read-only. Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY. This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="8d0bd-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-162">Indica el uso probable del documento; por ejemplo, un expediente de abogado.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="8d0bd-163">Esto puede corresponder a la plantilla de Office utilizada para crear el documento.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="8d0bd-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="8d0bd-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-166">Indica el tipo MIME del documento, que indica el formato como &quot;text/HTML&quot;'.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="8d0bd-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-169">Indica el idioma en el que se almacena el contenido.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="8d0bd-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p117">Sólo lectura.

Indica una estructura FILETIME que contiene la hora de creación del recurso.

El tiempo se indica en formato UTC (Horario universal coordinado).</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p117">Read-only. Indicates a FILETIME structure containing the time the resource was created. The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="8d0bd-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p118">Sólo lectura.

Indica una estructura FILETIME que contiene la hora del último acceso al recurso. La hora está en formato UTC. Los miembros de FILETIME son cero si el proveedor no admite este miembro de hora.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p118">Read-only. Indicates a FILETIME structure containing the time that the resource was last accessed. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="8d0bd-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p119">Sólo lectura.

Indica una estructura FILETIME que contiene la hora a la que se escribió el recurso por última vez.

La hora se especifica en formato UTC.

Los miembros de FILETIME son cero si el proveedor no admite este miembro de hora.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p119">Read-only. Indicates a FILETIME structure containing the time that the resource was last written. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="8d0bd-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="8d0bd-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p120">Sólo lectura.

Indica el tamaño, en bytes, de la secuencia predeterminada del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p120">Read-only. Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="8d0bd-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="8d0bd-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p121">Sólo lectura.

Es True si el recurso es una colección, como un directorio.

Es False si el recurso es un archivo simple.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p121">Read-only. True if the resource is a collection, such as a directory. False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="8d0bd-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="8d0bd-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p122">Es True si el recurso es un documento estructurado.

Es False si el recurso no es un documento estructurado.

Podría ser una colección o un archivo simple.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p122">True if the resource is a structured document. False if the resource is not a structured document. It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="8d0bd-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p123">Sólo lectura.

Indica que este recurso contiene una dirección URL al documento simple predeterminado de una carpeta o un documento estructurado.

Se utiliza cuando se solicita la secuencia predeterminada de un recurso.

Esta propiedad está en blanco en el caso de un archivo simple.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p123">Read-only. Indicates that this resource contains a URL to the default simple document of a folder or a structured document. Used when the default stream is requested from a resource. This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="8d0bd-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="8d0bd-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p124">Sólo lectura. Es opcional. Indica el capítulo del conjunto de filas que contiene los objetos secundarios del recurso. (<em>OLE DB Provider for Internet Publishing</em> no utiliza esta columna.)</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p124">Read-only. Optional. Indicates the chapter of the rowset containing the children of the resource. (The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0bd-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="8d0bd-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="8d0bd-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p125">Sólo lectura.

Indica el nombre para mostrar del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p125">Read-only. Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0bd-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="8d0bd-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="8d0bd-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="8d0bd-p126">Sólo lectura.

Es True si el recurso es la raíz de una colección o un documento estructurado.</span><span class="sxs-lookup"><span data-stu-id="8d0bd-p126">Read-only. True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>

