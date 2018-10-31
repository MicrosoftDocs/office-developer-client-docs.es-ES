---
title: CopyRecord (método, ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01141e0dc2445a91267cf7744214b906a1af3fd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860346"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="033e6-102">CopyRecord (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="033e6-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="033e6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="033e6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="033e6-104">Copia una entidad representada por un objeto **Record** en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="033e6-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="033e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="033e6-105">Syntax</span></span>

<span data-ttu-id="033e6-106">*Registro*. CopyRecord (*origen*, *destino*, *nombre de usuario*, *contraseña*, *Opciones*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="033e6-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="033e6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="033e6-107">Parameters</span></span>

  - <span data-ttu-id="033e6-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="033e6-108">*Source*</span></span>

  - <span data-ttu-id="033e6-109">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="033e6-109">Optional.</span></span> <span data-ttu-id="033e6-110">Valor de tipo **String** con la dirección URL que especifica la entidad que se va a copiar (por ejemplo, un archivo o directorio).</span><span class="sxs-lookup"><span data-stu-id="033e6-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="033e6-111">Si se omite *Source* o especifica una cadena vacía, se copiará el archivo o directorio representado por el actual [registro](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="033e6-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="033e6-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="033e6-112">*Destination*</span></span>

  - <span data-ttu-id="033e6-113">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="033e6-113">Optional.</span></span> <span data-ttu-id="033e6-114">Un valor de **tipo String** que contiene una dirección URL que especifica la ubicación donde se va a copiar *Source* .</span><span class="sxs-lookup"><span data-stu-id="033e6-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="033e6-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="033e6-115">*UserName*</span></span>

  - <span data-ttu-id="033e6-p103">Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.</span><span class="sxs-lookup"><span data-stu-id="033e6-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="033e6-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="033e6-118">*Password*</span></span>

  - <span data-ttu-id="033e6-p104">Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.</span><span class="sxs-lookup"><span data-stu-id="033e6-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="033e6-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="033e6-121">*Options*</span></span>

  - <span data-ttu-id="033e6-p105">Es opcional. Valor de [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tiene **adCopyUnspecified** como valor predeterminado. Especifica el comportamiento de este método.</span><span class="sxs-lookup"><span data-stu-id="033e6-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="033e6-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="033e6-125">*Async*</span></span>

  - <span data-ttu-id="033e6-p106">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.</span><span class="sxs-lookup"><span data-stu-id="033e6-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

<span data-ttu-id="033e6-128"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="033e6-128"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="033e6-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="033e6-129">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="033e6-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="033e6-130">Return value</span></span>
>>>>>>> <span data-ttu-id="033e6-131">master</span><span class="sxs-lookup"><span data-stu-id="033e6-131">master</span></span>

<span data-ttu-id="033e6-p107">Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="033e6-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="033e6-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="033e6-134">Remarks</span></span>

<span data-ttu-id="033e6-135">Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="033e6-135">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="033e6-136">Al menos uno de los nombres de servidor, ruta de acceso o recurso debe ser diferente.</span><span class="sxs-lookup"><span data-stu-id="033e6-136">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="033e6-p109">Todos los elementos secundarios de *Source* (por ejemplo, subdirectorios) se copian de forma recursiva, a menos que se especifique **adCopyNonRecursive**. En una operación recursiva, *Destination* no puede ser un subdirectorio de *Source*; en caso contrario, la operación no finalizará.</span><span class="sxs-lookup"><span data-stu-id="033e6-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="033e6-139">Este método se produce un error si *Destination* identifica una entidad existente (por ejemplo, un archivo o directorio), a menos que **se especifique adCopyOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="033e6-139">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="033e6-140">[!IMPORTANTE] Utilice la opción **adCopyOverWrite** con criterio.</span><span class="sxs-lookup"><span data-stu-id="033e6-140">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="033e6-141">Por ejemplo, si especifica esta opción cuando copia un archivo en un directorio va a *Eliminar* el directorio y reemplácelo con el archivo.</span><span class="sxs-lookup"><span data-stu-id="033e6-141">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>




> [!NOTE]
<span data-ttu-id="033e6-142"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="033e6-142"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="033e6-p111">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="033e6-p111">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="033e6-145">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="033e6-145">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="033e6-146">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="033e6-146">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="033e6-147">master</span><span class="sxs-lookup"><span data-stu-id="033e6-147">master</span></span>


