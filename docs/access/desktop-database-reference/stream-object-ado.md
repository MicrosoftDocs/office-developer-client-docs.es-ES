---
title: Stream (objeto, ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75e0422b6c6fcd2f893777884d35bade81a793f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997045"
---
# <a name="stream-object-ado"></a><span data-ttu-id="316bc-102">Stream (objeto, ADO)</span><span class="sxs-lookup"><span data-stu-id="316bc-102">Stream object (ADO)</span></span>


<span data-ttu-id="316bc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="316bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="316bc-104">Representa una secuencia de datos binarios o texto.</span><span class="sxs-lookup"><span data-stu-id="316bc-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="316bc-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="316bc-105">Remarks</span></span>

<span data-ttu-id="316bc-106">En jerarquías con estructura de árbol, como un sistema de archivos o en un sistema de correo electrónico, un [registro](record-object-ado.md) puede tener una secuencia binaria predeterminada de bits asociados que contiene el contenido del archivo o el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="316bc-106">In tree-structured hierarchies such as a file system or an email system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the email.</span></span> <span data-ttu-id="316bc-107">Un objeto **Stream** se puede usar para manipular campos o registros que contengan estas secuencias de datos.</span><span class="sxs-lookup"><span data-stu-id="316bc-107">A **Stream** object can be used to manipulate fields or records containing these streams of data.</span></span> <span data-ttu-id="316bc-108">Puede obtener un objeto **Stream** de estas maneras:</span><span class="sxs-lookup"><span data-stu-id="316bc-108">A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="316bc-p102">Desde una dirección URL que señala un objeto (normalmente un archivo) que contiene datos de texto o binarios. Este objeto puede ser un documento simple, un objeto **Record** que representa un documento estructurado, o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="316bc-p102">From a URL pointing to an object (typically a file) containing binary or text data. This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="316bc-p103">Abriendo el objeto **Stream** predeterminado asociado a un objeto **Record**. Se puede obtener la secuencia predeterminada asociada al objeto **Record** cuando se abre el objeto **Record**, para eliminar un viaje de ida y vuelta en el momento de abrir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="316bc-p103">By opening the default **Stream** object associated with a **Record** object. You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="316bc-p104">Creando instancias de un objeto **Stream**. Estos objetos **Stream** se pueden utilizar para almacenar datos necesarios para la aplicación. A diferencia de un objeto **Stream** asociado a una dirección URL, o el objeto **Stream** predeterminado de un objeto **Record**, un objeto **Stream** del que se han creado instancias no tiene asociación a un origen subyacente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="316bc-p104">By instantiating a **Stream** object. These **Stream** objects can be used to store data for the purposes of your application. Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="316bc-116">Con los métodos y las propiedades de un objeto **Stream**, se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="316bc-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="316bc-117">Abrir un objeto **Stream** desde un objeto **Record** o una dirección URL con el método [Open](open-method-ado-stream.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="316bc-118">Cerrar un objeto **Stream** con el método [Close](close-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="316bc-119">Especificar bytes o texto en un objeto **Stream** con los métodos [Write](write-method-ado.md) y [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="316bc-120">Leer bytes del objeto **Stream** con los métodos [Read](read-method-ado.md) y [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="316bc-121">Escribir datos del objeto **Stream**, que están todavía en el búfer de ADO, en el objeto subyacente con el método [Flush](flush-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="316bc-122">Copiar el contenido de un objeto **Stream** en otro objeto **Stream** con el método [CopyTo](copyto-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="316bc-123">Controlar cómo se leen las líneas del archivo de origen con el método [SkipLine](skipline-method-ado.md) y la propiedad [LineSeparator](lineseparator-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="316bc-124">Determinar el fin de la secuencia con la propiedad [EOS](eos-property-ado.md) y el método [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="316bc-125">Guardar y restaurar datos en archivos con los métodos [SaveToFile](savetofile-method-ado.md) y [LoadFromFile](loadfromfile-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="316bc-126">Especificar el juego de caracteres usado para almacenar el objeto **Stream** con la propiedad [Charset](charset-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="316bc-127">Detener una operación asincrónica del objeto **Stream** con el método [Cancel](cancel-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="316bc-128">Determinar el número de bytes de un objeto **Stream** con la propiedad [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="316bc-128">Determine the number of bytes in a **Stream** with the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="316bc-129">Controlar la posición actual dentro de un objeto **Stream** con la propiedad [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="316bc-130">Determinar el tipo de datos de un objeto **Stream** con la propiedad [Type](type-property-ado-stream.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="316bc-131">Determinar el estado actual del objeto **Stream** (cerrado, abierto o en ejecución) con la propiedad [State](state-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="316bc-132">Especificar el modo de acceso para el objeto **Stream** con la propiedad [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>

> [!NOTE]
> <span data-ttu-id="316bc-133">[!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-133">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="316bc-134">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="316bc-134">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


