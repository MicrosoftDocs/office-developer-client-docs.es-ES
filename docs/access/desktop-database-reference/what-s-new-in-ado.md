---
title: Novedades de ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302614"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="5cfaa-102">Novedades de ADO</span><span class="sxs-lookup"><span data-stu-id="5cfaa-102">What's new in ADO</span></span>

<span data-ttu-id="5cfaa-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cfaa-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="5cfaa-104">ADO 2.5 incluye las siguientes características nuevas y una documentación mejorada.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="5cfaa-105">Esta lista hace referencia a ADO, ADO MD y ADOX.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="5cfaa-106">Características nuevas</span><span class="sxs-lookup"><span data-stu-id="5cfaa-106">New features</span></span>

- <span data-ttu-id="5cfaa-107">**[Registros y secuencias](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="5cfaa-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="5cfaa-108">Esta versión de ADO introduce el objeto [Record](record-object-ado.md) , que puede representar y administrar elementos como directorios y archivos en un sistema de archivos, y carpetas y mensajes en un sistema de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="5cfaa-109">Un objeto **Record** también puede representar una fila en un objeto [Recordset](recordset-object-ado.md), si bien los objetos **Record** y **Recordset** tienen métodos y propiedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="5cfaa-110">El nuevo objeto [Stream](stream-object-ado.md) permite leer, escribir y administrar la secuencia binaria de bytes o texto que componen una secuencia de archivos o mensajes.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="5cfaa-111">**[Uso de dirección URL](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="5cfaa-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="5cfaa-p103">Esta versión también introduce el uso de Localizadores uniformes de recursos (URL), como alternativa a las cadenas de conexión y texto de comando, para denominar los objetos de un almacén de datos. Estos localizadores se pueden usar con los objetos [Connection](connection-object-ado.md) y **Recordset** existentes, así como con los nuevos objetos **Record** y **Stream**.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="5cfaa-p104">Con esta versión, ADO admite proveedores OLE DB que reconocen sus propios esquemas URL. Por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* que obtiene acceso al sistema de archivos de Windows 2000, reconoce el esquema HTTP existente.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-p104">With this release, ADO supports OLE DB providers that recognize their own URL schemes. For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="5cfaa-116">**[Campos especiales para proveedores de orígenes de documentos](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="5cfaa-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="5cfaa-117">Una clase especial de proveedores, denominados proveedores de *orígenes de documentos*, administran carpetas y documentos.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="5cfaa-118">Cuando un objeto **Record** representa un documento, o un objeto **Recordset** representa una carpeta de documentos, el proveedor de orígenes de documentos rellena esos objetos con un conjunto único de campos que describen las características del documento.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="5cfaa-119">Estos campos constituyen un objeto **Record** o **Recordset**de *recurso* .</span><span class="sxs-lookup"><span data-stu-id="5cfaa-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="5cfaa-120">Nuevos temas de referencia</span><span class="sxs-lookup"><span data-stu-id="5cfaa-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="5cfaa-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5cfaa-121">Properties</span></span>

<span data-ttu-id="5cfaa-122">Esta versión incluye las siguientes propiedades nuevas.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cfaa-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5cfaa-123">Property</span></span></p></th>
<th><p><span data-ttu-id="5cfaa-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cfaa-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-125"><a href="charset-property-ado.md">Juego</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-126">Indica el juego de caracteres al que debe convertirse el contenido de un objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-127"><a href="eos-property-ado.md">OCASIONA</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-128">Indica si la posición actual se encuentra al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-130">Indica el carácter binario que se va a utilizar como separador de línea en los objetos <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-132">Indica los permisos disponibles para modificar los datos de un objeto <strong>Connection</strong>, <strong>Record</strong> o <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-134">Indica una cadena URL absoluta que señala el objeto <strong>Record</strong> primario del actual objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-136">Indica la posición actual dentro de un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-138">Indica el tipo de objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-140">Indica el tamaño de la secuencia en número de bytes.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-142">Indica la entidad representada por el objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-144">Indica, para todos los objetos aplicables, si el estado del objeto es abierto o cerrado.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="5cfaa-145">Indica para todos los objetos aplicables que ejecutan un método asincrónico si el objeto se encuentra actualmente en estado de conexión, ejecución o recuperación.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-146"><a href="type-property-ado-stream.md">Type</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-147">Indica el tipo de datos incluidos en el objeto <strong>Stream</strong> (binario o de texto).</span><span class="sxs-lookup"><span data-stu-id="5cfaa-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="5cfaa-148">Métodos</span><span class="sxs-lookup"><span data-stu-id="5cfaa-148">Methods</span></span>

<span data-ttu-id="5cfaa-149">Esta versión incluye los siguientes métodos nuevos.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cfaa-150">Método</span><span class="sxs-lookup"><span data-stu-id="5cfaa-150">Method</span></span></p></th>
<th><p><span data-ttu-id="5cfaa-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cfaa-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-153">Copia un archivo o directorio y su contenidos en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-155">Copia el número especificado de caracteres o bytes (según el <strong>tipo</strong>) del <strong>objeto</strong> <strong>Stream</strong> en otro objeto <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cfaa-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-157">Elimina un archivo o directorio y todos sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-158"><a href="flush-method-ado.md">Limpia</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-159">Vacía el contenido del objeto <strong>Stream</strong> que permanece en el búfer de ADO en el objeto subyacente al que está asociado el objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-161">Devuelve un objeto <strong>Recordset</strong> cuyas filas representan los archivos y subdirectorios del directorio representado por este objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-163">Carga el contenido de un archivo existente en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-165">Mueve un archivo o directorio y su contenido a otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-167">Abre un objeto <strong>Record</strong> existente o crea un nuevo archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-169">Abre un objeto <strong>Stream</strong> para manipular secuencias de datos binarios o de texto.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-170"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-171">Lee un número especificado de bytes de un objeto <strong>Stream</strong> binario.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-172"><a href="readtext-method-ado.md">Dtex</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-173">Lee un número especificado de caracteres de un objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-175">Guarda el contenido binario de un objeto <strong>Stream</strong> en un archivo.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-177">Establece la posición que es el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-179">Omite una línea completa al leer un objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cfaa-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-181">Escribe datos binarios en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cfaa-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="5cfaa-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="5cfaa-183">Escribe una cadena de texto especificada en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="5cfaa-184">Documentación nueva y mejorada</span><span class="sxs-lookup"><span data-stu-id="5cfaa-184">New and enhanced documentation</span></span>

- <span data-ttu-id="5cfaa-185">**[Temas de ejemplo de código](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="5cfaa-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="5cfaa-186">Los ejemplos se han expandido para contener ejemplos de código escritos en Microsoft Visual C++ y Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="5cfaa-187">Estos ejemplos de código se pueden copiar y pegar en el editor.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="5cfaa-188">**[Temas de proveedores](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="5cfaa-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="5cfaa-189">Se ha incluido un tema nuevo en el que se explica cómo utilizar ADO con [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="5cfaa-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="5cfaa-190">**[Programar con ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="5cfaa-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="5cfaa-191">Esta nueva sección contiene sugerencias y trucos para usar ADO con varios lenguajes de programación.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="5cfaa-192">Contiene los índices de sintaxis existentes para las extensiones de Visual C++ para ADO y ADO/WFC, así como nueva información específica para los programadores que utilizan Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ o Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="5cfaa-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

