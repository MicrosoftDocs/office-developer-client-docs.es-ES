---
title: MoveRecord (método, ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5aab77571b0b12c6b26cd15af386c9ee89162681
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930018"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="5604a-102">MoveRecord (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="5604a-102">MoveRecord method (ADO)</span></span>


<span data-ttu-id="5604a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5604a-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="5604a-104">Mueve a otra ubicación la entidad representada por un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5604a-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="5604a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5604a-105">Syntax</span></span>

<span data-ttu-id="5604a-106">*Registro*. MoveRecord (*origen*, *destino*, *nombre de usuario*, *contraseña*, *Opciones*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="5604a-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5604a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5604a-107">Parameters</span></span>

  - <span data-ttu-id="5604a-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="5604a-108">*Source*</span></span>

  - <span data-ttu-id="5604a-p101">Es opcional. Valor de tipo **String** con una dirección URL que identifica el objeto **Record** que se va a mover. Si se omite *Source* o se especifica una cadena vacía, se mueve el objeto representado por este objeto **Record**. Por ejemplo, si el objeto **Record** representa un archivo, el contenido del archivo se mueve hacia la ubicación especificada por *Destination*.</span><span class="sxs-lookup"><span data-stu-id="5604a-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="5604a-113">*Destination*</span><span class="sxs-lookup"><span data-stu-id="5604a-113">*Destination*</span></span>

  - <span data-ttu-id="5604a-114">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="5604a-114">Optional.</span></span> <span data-ttu-id="5604a-115">Un valor de **tipo String** que contiene una dirección URL que especifica la ubicación donde se va a mover *Source* .</span><span class="sxs-lookup"><span data-stu-id="5604a-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="5604a-116">*UserName*</span><span class="sxs-lookup"><span data-stu-id="5604a-116">*UserName*</span></span>

  - <span data-ttu-id="5604a-p103">Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.</span><span class="sxs-lookup"><span data-stu-id="5604a-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="5604a-119">*Password*</span><span class="sxs-lookup"><span data-stu-id="5604a-119">*Password*</span></span>

  - <span data-ttu-id="5604a-p104">Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.</span><span class="sxs-lookup"><span data-stu-id="5604a-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="5604a-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="5604a-122">*Options*</span></span>

  - <span data-ttu-id="5604a-p105">Es opcional. Valor de [MoveRecordOptionsEnum](moverecordoptionsenum.md), cuyo valor predeterminado es **adMoveUnspecified**. Especifica el comportamiento de este método.</span><span class="sxs-lookup"><span data-stu-id="5604a-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="5604a-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="5604a-126">*Async*</span></span>

  - <span data-ttu-id="5604a-p106">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5604a-p106">Optional. A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

## <a name="return-value"></a><span data-ttu-id="5604a-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5604a-129">Return value</span></span>

<span data-ttu-id="5604a-130">Valor de tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="5604a-130">A **String** value.</span></span> <span data-ttu-id="5604a-131">Normalmente, se devuelve el valor de *destino* .</span><span class="sxs-lookup"><span data-stu-id="5604a-131">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="5604a-132">Sin embargo, el valor devuelto exacto depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5604a-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="5604a-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5604a-133">Remarks</span></span>

<span data-ttu-id="5604a-134">Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5604a-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="5604a-135">Al menos los nombres de servidor, ruta de acceso o recurso deben ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="5604a-135">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="5604a-p109">En el caso de los archivos que se mueven mediante el proveedor de publicaciones en Internet, este método actualiza todos los vínculos de hipertexto en los archivos que se están moviendo, a menos que se especifique lo contrario en *Options*. Este método genera un error si *Destination* identifica un objeto existente (por ejemplo, un archivo o directorio), a menos que se especifique **adMoveOverWrite**.</span><span class="sxs-lookup"><span data-stu-id="5604a-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5604a-p110">[!NOTA] Utilice la opción <STRONG>adMoveOverWrite</STRONG> con criterio. Por ejemplo, si especifica esta opción cuando mueve un archivo a un directorio, se eliminará el directorio y se reemplazará con el archivo.</span><span class="sxs-lookup"><span data-stu-id="5604a-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="5604a-p111">Algunos atributos del objeto **Record**, como la propiedad [ParentURL](parenturl-property-ado.md), no se actualizarán tras finalizar esta operación. Actualice las propiedades del objeto **Record** cerrando el objeto **Record** y abriéndolo de nuevo con la dirección URL de la ubicación a la que se ha movido el archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="5604a-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="5604a-p112">Si este objeto **Record** se ha obtenido de un objeto [Recordset](recordset-object-ado.md), la nueva ubicación del archivo o directorio que se ha movido no se reflejará inmediatamente en el objeto **Recordset**. Actualice el objeto **Recordset** cerrando y abriéndolo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="5604a-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <span data-ttu-id="5604a-144">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="5604a-144">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="5604a-145">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="5604a-145">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


