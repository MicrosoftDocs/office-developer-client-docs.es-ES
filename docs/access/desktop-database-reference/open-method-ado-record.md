---
title: Open (método, objeto Record de ADO)
TOCTitle: Open Method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f29f707f02ed8adbf2b1881b0721ce912b278353
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605831"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="564eb-102">Open (método, objeto Record de ADO)</span><span class="sxs-lookup"><span data-stu-id="564eb-102">Open Method (ADO Record)</span></span>


<span data-ttu-id="564eb-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="564eb-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="564eb-104">Abre un objeto [Record](record-object-ado.md) existente o crea un nuevo elemento representado por el objeto **Record** (como un archivo o un directorio).</span><span class="sxs-lookup"><span data-stu-id="564eb-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="564eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="564eb-105">Syntax</span></span>

<span data-ttu-id="564eb-106">Abrir *origen*, *ActiveConnection*, *modo*, *CreateOptions*, *Opciones*, *nombre de usuario*, *contraseña*</span><span class="sxs-lookup"><span data-stu-id="564eb-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="564eb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="564eb-107">Parameters</span></span>

  - <span data-ttu-id="564eb-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="564eb-108">*Source*</span></span>

  - <span data-ttu-id="564eb-p101">Es opcional. **Variant** que puede representar la dirección URL de la entidad que va a representar este objeto **Record**, un objeto **Command**, un objeto [Recordset](recordset-object-ado.md) abierto u otro objeto **Record**, una cadena que contiene una instrucción SQL SELECT o un nombre de tabla.</span><span class="sxs-lookup"><span data-stu-id="564eb-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>

  - <span data-ttu-id="564eb-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="564eb-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="564eb-p102">Es opcional. **Variant** que representa la cadena de conexión o el objeto [Connection](connection-object-ado.md) abierto.</span><span class="sxs-lookup"><span data-stu-id="564eb-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="564eb-114">*Mode*</span><span class="sxs-lookup"><span data-stu-id="564eb-114">*Mode*</span></span>

  - <span data-ttu-id="564eb-p103">Es opcional. Valor de [ConnectModeEnum](connectmodeenum.md), cuyo valor predeterminado es **adModeUnknown**, que especifica el modo de acceso del objeto **Record** resultante.</span><span class="sxs-lookup"><span data-stu-id="564eb-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>

  - <span data-ttu-id="564eb-117">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="564eb-117">*CreateOptions*</span></span>

  - <span data-ttu-id="564eb-118">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="564eb-118">Optional.</span></span> <span data-ttu-id="564eb-119">Valor de [RecordCreateOptionsEnum](recordcreateoptionsenum.md), cuyo valor predeterminado es **adFailIfNotExists**, que especifica si debe haber un archivo o directorio abierto o si debe crearse un nuevo archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="564eb-119">A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</span></span> <span data-ttu-id="564eb-120">Si está especificado el valor predeterminado, el modo de acceso se obtiene de la propiedad [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="564eb-120">If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property.</span></span> <span data-ttu-id="564eb-121">Este parámetro se omite cuando el parámetro *Source* no contiene una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="564eb-121">This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>

  - <span data-ttu-id="564eb-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="564eb-122">*Options*</span></span>

  - <span data-ttu-id="564eb-p105">Es opcional. Valor de [RecordOpenOptionsEnum](recordopenoptionsenum.md), cuyo valor predeterminado es **adOpenRecordUnspecified**, que especifica las opciones para abrir el objeto **Record**. Estos valores se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="564eb-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>

  - <span data-ttu-id="564eb-126">*UserName*</span><span class="sxs-lookup"><span data-stu-id="564eb-126">*UserName*</span></span>

  - <span data-ttu-id="564eb-p106">Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Source*.</span><span class="sxs-lookup"><span data-stu-id="564eb-p106">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>

  - <span data-ttu-id="564eb-129">*Password*</span><span class="sxs-lookup"><span data-stu-id="564eb-129">*Password*</span></span>

  - <span data-ttu-id="564eb-p107">Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.</span><span class="sxs-lookup"><span data-stu-id="564eb-p107">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

## <a name="remarks"></a><span data-ttu-id="564eb-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="564eb-132">Remarks</span></span>

<span data-ttu-id="564eb-133">*Source* puede ser:</span><span class="sxs-lookup"><span data-stu-id="564eb-133">*Source* may be:</span></span>

  - <span data-ttu-id="564eb-134">Una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="564eb-134">A URL.</span></span> <span data-ttu-id="564eb-135">Si el protocolo de la dirección URL es http, se invocará de forma predeterminada el proveedor de Internet.</span><span class="sxs-lookup"><span data-stu-id="564eb-135">If the protocol for the URL is http, then the Internet Provider will be invoked by default.</span></span> <span data-ttu-id="564eb-136">Si la dirección URL señala un nodo que contiene un script ejecutable (como una página .ASP), se abre de manera predeterminada un objeto **Record** que contiene el origen en lugar del contenido ejecutado.</span><span class="sxs-lookup"><span data-stu-id="564eb-136">If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default.</span></span> <span data-ttu-id="564eb-137">Use el argumento *Options* para modificar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="564eb-137">Use the *Options* argument to modify this behavior.</span></span>

  - <span data-ttu-id="564eb-p109">Un objeto **Record**. Un objeto **Record** que se abre desde otro objeto **Record** duplicará el objeto **Record** original.</span><span class="sxs-lookup"><span data-stu-id="564eb-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

  - <span data-ttu-id="564eb-p110">Un objeto **Command**. El objeto **Record** abierto representa la fila devuelta por la ejecución del objeto **Command**. Si los resultados contienen más de una fila, el contenido de la primera fila se ubica en el registro y puede que se agregue un error a la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="564eb-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="564eb-p111">Una instrucción SQL SELECT. El objeto **Record** abierto representa la fila devuelta por la ejecución del contenido de la cadena. Si los resultados contienen más de una fila, el contenido de la primera fila se ubica en el registro y puede que se agregue un error a la colección **Errors**.</span><span class="sxs-lookup"><span data-stu-id="564eb-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="564eb-146">Un nombre de tabla.</span><span class="sxs-lookup"><span data-stu-id="564eb-146">A table name.</span></span>

<span data-ttu-id="564eb-147">Si el objeto **Record** representa una entidad a la que no se puede obtener acceso con una dirección URL (por ejemplo, una fila de un objeto **Recordset** derivado de una base de datos), los valores de la propiedad [ParentURL](parenturl-property-ado.md) y del campo al que se obtiene acceso con la constante **adRecordURL** son null.</span><span class="sxs-lookup"><span data-stu-id="564eb-147">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>


> [!NOTE]
<span data-ttu-id="564eb-148"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="564eb-148"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="564eb-p112">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="564eb-p112">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="564eb-151">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="564eb-151">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="564eb-152">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="564eb-152">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="564eb-153">master</span><span class="sxs-lookup"><span data-stu-id="564eb-153">master</span></span>


