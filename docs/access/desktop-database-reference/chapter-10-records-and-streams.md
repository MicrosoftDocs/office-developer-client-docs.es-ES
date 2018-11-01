---
title: 'Capítulo 10: Registros y flujos'
TOCTitle: 'Chapter 10: Records and Streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c61aef7a4f0cc34f256300304823341c99fb8436
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876970"
---
# <a name="chapter-10-records-and-streams"></a><span data-ttu-id="92669-102">Capítulo 10: Registros y flujos</span><span class="sxs-lookup"><span data-stu-id="92669-102">Chapter 10: Records and Streams</span></span>


<span data-ttu-id="92669-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92669-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92669-p101">ADO proporciona actualmente el objeto [Recordset](recordset-object-ado.md) como medio principal de obtener acceso a información que se encuentra en orígenes de datos, tales como las bases de datos relacionales. No obstante, algunos proveedores admiten los objetos [Record](record-object-ado.md) y [Stream](stream-object-ado.md) como objetos alternativos o complementarios para manipular los datos. Para obtener información más específica sobre el comportamiento del objeto **Recordset**, vea la documentación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="92669-p101">ADO currently provides the[Recordset](recordset-object-ado.md) object as the primary means of accessing information in data sources, such as relational databases. However, some providers support the [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects as alternative or complementary objects with which data from providers can be manipulated. For specifics on **Record** behavior, see your provider's documentation.</span></span>

## <a name="records"></a><span data-ttu-id="92669-107">Objetos Record</span><span class="sxs-lookup"><span data-stu-id="92669-107">Records</span></span>

<span data-ttu-id="92669-p102">Los objetos **Record** funcionan básicamente como objetos **Recordset** de una fila. Sin embargo, los **Records** presentan una funcionalidad limitada en comparación con los **Recordsets** y tienen propiedades y métodos diferentes. El origen para los datos de un objeto **Record** puede ser un comando que devuelva una fila de datos desde el proveedor. El uso de objetos **Record** en vez de **Recordset** para recibir los resultados de una consulta que devuelve una fila de datos elimina la sobrecarga de crear instancias del objeto **Recordset** (más complejo).</span><span class="sxs-lookup"><span data-stu-id="92669-p102">**Record** objects essentially function as one-row **Recordset**s. However, **Records** have limited functionality compared to **Recordsets** and they have different properties and methods.The source for the data in a **Record** object can be a command which returns one row of data from the provider. Using **Record** objects rather than **Recordset** objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex **Recordset** object.</span></span>

<span data-ttu-id="92669-p103">Los objetos **Record** pueden servir para otro propósito, especialmente con proveedores para orígenes de datos distintos de las bases de datos relacionales tradicionales, tales como [ Microsoft OLE DB Provider for Internet Publishing ](microsoft-ole-db-provider-for-internet-publishing.md). Gran parte de la información que se debe procesar existe no como tablas de bases de datos, sino como mensajes de sistemas de correo electrónico o como archivos de los modernos sistemas de archivos. Los objetos **Record** y **Stream** facilitan el acceso a información almacenada en orígenes distintos de las bases de datos relacionales.</span><span class="sxs-lookup"><span data-stu-id="92669-p103">**Record** objects can serve another purpose, particularly with providers for data sources other than traditional relational databases, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Much of the information that must be processed exists, not as tables in databases, but as messages in electronic mail systems and files in modern file systems. The **Record** and **Stream** objects facilitate access to information stored in sources other than relational databases.</span></span>

<span data-ttu-id="92669-p104">El objeto **Record** puede representar y administrar datos tales como directorios y archivos de un sistema de archivos, o carpetas y mensajes de un sistema de correo electrónico. En estos casos, el origen para el **registro** puede ser la fila actual de un objeto **Recordset** abierto, una dirección URL absoluta o una dirección URL relativa en combinación con un objeto [Connection](connection-object-ado.md) abierto.</span><span class="sxs-lookup"><span data-stu-id="92669-p104">The **Record** object can represent and manage data such as directories and files in a file system or folders and messages in an e-mail system. For these purposes, the source for the **Record** can be the current row of an open **Recordset**, an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="92669-p105">Normalmente, un objeto **Recordset** se puede usar para representar un contenedor o un elemento principal de una jerarquía, tal como una carpeta o un directorio. Un **registro** se puede usar para devolver información específica sobre un nodo del contenedor principal, tal como un archivo o documento. La razón principal por la que los objetos **Record** se utilizan para representar este tipo de información es que estos orígenes de datos son heterogéneos. Esto significa que cada **registro** puede tener un conjunto y un número diferente de campos. Los objetos **Recordset** usuales que contienen filas de una base de datos son homogéneos, lo cual significa que cada fila tiene el mismo número y tipo de campos.</span><span class="sxs-lookup"><span data-stu-id="92669-p105">Typically, a **Recordset** can be used to represent a container or parent in a hierarchy such as a folder or directory. A **Record** can be used to return specific information about one node in the parent container, such as a file or document. The primary reason **Records** are used to represent this type of information is that these sources of data are heterogenous. This means that each **Record** may have a different set and number of fields. Traditional **Recordsets** containing rows from a database are homogenous, which means that each row has the same number and type of fields.</span></span>

<span data-ttu-id="92669-121">Si desea obtener más información acerca del uso del objeto **Record** para procesar datos heterogéneos de proveedores como el Proveedor de publicación en Internet, vea [Uso de ADO para publicación en Internet](using-ado-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="92669-121">For more information about using the **Record** object for processing this heterogeneous data from providers such as the Internet Publishing Provider, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

## <a name="streams"></a><span data-ttu-id="92669-122">Objetos Stream</span><span class="sxs-lookup"><span data-stu-id="92669-122">Streams</span></span>

<span data-ttu-id="92669-p106">El objeto **Stream** proporciona el medio para leer, escribir y administrar una secuencia de bytes. Esta secuencia de bytes puede ser texto o datos binarios, y su tamaño sólo está limitada por los recursos del sistema. Los objetos **Stream** de ADO se suelen utilizar para los propósitos siguientes:</span><span class="sxs-lookup"><span data-stu-id="92669-p106">The **Stream** object provides the means to read, write, and manage a stream of bytes. This byte stream may be text or binary and is limited in size only by system resources. Typically, ADO **Stream** objects are used for the following purposes:</span></span>

  - <span data-ttu-id="92669-p107">Contener el texto o los bytes que componen un archivo o un mensaje (normalmente se utiliza con proveedores tales como el Microsoft OLE DB Provider for Internet Publishing. Si desea obtener más información acerca de este uso de los objetos **Stream**, vea [Uso de ADO para publicación en Internet](using-ado-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="92669-p107">To contain the text or bytes that comprise a file or message, typically used with providers such as the Microsoft OLE DB Provider for Internet Publishing. For more information about this use of **Stream** objects, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

<span data-ttu-id="92669-128">Un objeto **Stream** se puede abrir sobre:</span><span class="sxs-lookup"><span data-stu-id="92669-128">A **Stream** object can be opened on:</span></span>

  - <span data-ttu-id="92669-129">Un archivo simple especificado con una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="92669-129">A simple file specified with a URL.</span></span>

  - <span data-ttu-id="92669-130">Un campo de un objeto **Record** o un objeto **Recordset** que contiene un objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="92669-130">A field of a **Record** or **Recordset** containing a **Stream** object.</span></span>

  - <span data-ttu-id="92669-131">La secuencia predeterminada de un objeto **Record** o **Recordset** que representa un directorio o un archivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="92669-131">The default stream of a **Record** or **Recordset** object representing a directory or compound file.</span></span>

  - <span data-ttu-id="92669-132">Un campo de recurso que contiene la dirección URL de un archivo simple.</span><span class="sxs-lookup"><span data-stu-id="92669-132">A resource field containing the URL of a simple file.</span></span>

  - <span data-ttu-id="92669-p108">Ninguna origen determinado. En este caso, el objeto **Stream** se abre en la memoria. Se pueden escribir datos en él y después guardarlos en otro **Stream** o en un archivo.</span><span class="sxs-lookup"><span data-stu-id="92669-p108">No particular source at all. In this case, a **Stream** object is opened in memory. Data can be written to it and then saved in another **Stream** or file.</span></span>

  - <span data-ttu-id="92669-136">Un campo BLOB de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="92669-136">A BLOB field in a **Recordset**.</span></span>

<span data-ttu-id="92669-137">En este capítulo, se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="92669-137">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="92669-138">Flujos y persistencia</span><span class="sxs-lookup"><span data-stu-id="92669-138">Streams and Persistence</span></span>](streams-and-persistence.md)

- [<span data-ttu-id="92669-139">Registros y campos proporcionados por el proveedor</span><span class="sxs-lookup"><span data-stu-id="92669-139">Records and Provider-Supplied Fields</span></span>](records-and-provider-supplied-fields.md)

- [<span data-ttu-id="92669-140">Direcciones URL relativas y absolutas</span><span class="sxs-lookup"><span data-stu-id="92669-140">Absolute and Relative URLs</span></span>](absolute-and-relative-urls.md)

- [<span data-ttu-id="92669-141">Using ADO for Internet Publishing (ADO)</span><span class="sxs-lookup"><span data-stu-id="92669-141">Using ADO for Internet Publishing (ADO)</span></span>](using-ado-for-internet-publishing.md)