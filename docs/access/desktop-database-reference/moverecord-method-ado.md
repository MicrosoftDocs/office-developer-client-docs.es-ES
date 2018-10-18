---
title: MoveRecord (método, ADO)
TOCTitle: MoveRecord Method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6955bca1bf693386d1f5edb4bac04cee311d78e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606965"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="5b315-102">MoveRecord (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="5b315-102">MoveRecord Method (ADO)</span></span>


<span data-ttu-id="5b315-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b315-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="5b315-104">Mueve a otra ubicación la entidad representada por un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5b315-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b315-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b315-105">Syntax</span></span>

<span data-ttu-id="5b315-106">*Registro*. MoveRecord (*origen*, *destino*, *nombre de usuario*, *contraseña*, *Opciones*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="5b315-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5b315-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b315-107">Parameters</span></span>

  - <span data-ttu-id="5b315-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="5b315-108">*Source*</span></span>

  - <span data-ttu-id="5b315-p101">Es opcional. Valor de tipo **String** con una dirección URL que identifica el objeto **Record** que se va a mover. Si se omite *Source* o se especifica una cadena vacía, se mueve el objeto representado por este objeto **Record**. Por ejemplo, si el objeto **Record** representa un archivo, el contenido del archivo se mueve hacia la ubicación especificada por *Destination*.</span><span class="sxs-lookup"><span data-stu-id="5b315-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="5b315-113">*Destination*</span><span class="sxs-lookup"><span data-stu-id="5b315-113">*Destination*</span></span>

  - <span data-ttu-id="5b315-114">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="5b315-114">Optional.</span></span> <span data-ttu-id="5b315-115">Un valor de **tipo String** que contiene una dirección URL que especifica la ubicación donde se va a mover *Source* .</span><span class="sxs-lookup"><span data-stu-id="5b315-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="5b315-116">*UserName*</span><span class="sxs-lookup"><span data-stu-id="5b315-116">*UserName*</span></span>

  - <span data-ttu-id="5b315-p103">Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.</span><span class="sxs-lookup"><span data-stu-id="5b315-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="5b315-119">*Password*</span><span class="sxs-lookup"><span data-stu-id="5b315-119">*Password*</span></span>

  - <span data-ttu-id="5b315-p104">Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.</span><span class="sxs-lookup"><span data-stu-id="5b315-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="5b315-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="5b315-122">*Options*</span></span>

  - <span data-ttu-id="5b315-p105">Es opcional. Valor de [MoveRecordOptionsEnum](moverecordoptionsenum.md), cuyo valor predeterminado es **adMoveUnspecified**. Especifica el comportamiento de este método.</span><span class="sxs-lookup"><span data-stu-id="5b315-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="5b315-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="5b315-126">*Async*</span></span>

  - <span data-ttu-id="5b315-p106">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5b315-p106">Optional. A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

<span data-ttu-id="5b315-129"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5b315-129"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5b315-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b315-130">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5b315-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b315-131">Return value</span></span>
>>>>>>> <span data-ttu-id="5b315-132">master</span><span class="sxs-lookup"><span data-stu-id="5b315-132">master</span></span>

<span data-ttu-id="5b315-133">Valor de tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="5b315-133">A **String** value.</span></span> <span data-ttu-id="5b315-134">Normalmente, se devuelve el valor de *destino* .</span><span class="sxs-lookup"><span data-stu-id="5b315-134">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="5b315-135">Sin embargo, el valor devuelto exacto depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5b315-135">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b315-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b315-136">Remarks</span></span>

<span data-ttu-id="5b315-137">Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5b315-137">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="5b315-138">Al menos los nombres de servidor, ruta de acceso o recurso deben ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="5b315-138">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="5b315-p109">En el caso de los archivos que se mueven mediante el proveedor de publicaciones en Internet, este método actualiza todos los vínculos de hipertexto en los archivos que se están moviendo, a menos que se especifique lo contrario en *Options*. Este método genera un error si *Destination* identifica un objeto existente (por ejemplo, un archivo o directorio), a menos que se especifique **adMoveOverWrite**.</span><span class="sxs-lookup"><span data-stu-id="5b315-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5b315-p110">[!NOTA] Utilice la opción <STRONG>adMoveOverWrite</STRONG> con criterio. Por ejemplo, si especifica esta opción cuando mueve un archivo a un directorio, se eliminará el directorio y se reemplazará con el archivo.</span><span class="sxs-lookup"><span data-stu-id="5b315-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="5b315-p111">Algunos atributos del objeto **Record**, como la propiedad [ParentURL](parenturl-property-ado.md), no se actualizarán tras finalizar esta operación. Actualice las propiedades del objeto **Record** cerrando el objeto **Record** y abriéndolo de nuevo con la dirección URL de la ubicación a la que se ha movido el archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="5b315-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="5b315-p112">Si este objeto **Record** se ha obtenido de un objeto [Recordset](recordset-object-ado.md), la nueva ubicación del archivo o directorio que se ha movido no se reflejará inmediatamente en el objeto **Recordset**. Actualice el objeto **Recordset** cerrando y abriéndolo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="5b315-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
<span data-ttu-id="5b315-147"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="5b315-147"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="5b315-p113">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="5b315-p113">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="5b315-150">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="5b315-150">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="5b315-151">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="5b315-151">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="5b315-152">master</span><span class="sxs-lookup"><span data-stu-id="5b315-152">master</span></span>


