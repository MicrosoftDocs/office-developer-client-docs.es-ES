---
title: CopyRecord (método, ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700832"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="7bf10-102">CopyRecord (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="7bf10-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="7bf10-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bf10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bf10-104">Copia una entidad representada por un objeto **Record** en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="7bf10-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bf10-105">Syntax</span></span>

<span data-ttu-id="7bf10-106">*Registro*. CopyRecord (*origen*, *destino*, *nombre de usuario*, *contraseña*, *Opciones*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="7bf10-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7bf10-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bf10-107">Parameters</span></span>

|<span data-ttu-id="7bf10-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7bf10-108">Parameter</span></span>|<span data-ttu-id="7bf10-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bf10-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7bf10-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="7bf10-110">*Source*</span></span> |<span data-ttu-id="7bf10-111">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="7bf10-111">Optional.</span></span> <span data-ttu-id="7bf10-112">Valor de tipo **String** con la dirección URL que especifica la entidad que se va a copiar (por ejemplo, un archivo o directorio).</span><span class="sxs-lookup"><span data-stu-id="7bf10-112">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="7bf10-113">Si se omite *Source* o especifica una cadena vacía, se copiará el archivo o directorio representado por el actual [registro](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7bf10-113">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="7bf10-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="7bf10-114">*Destination*</span></span> |<span data-ttu-id="7bf10-115">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="7bf10-115">Optional.</span></span> <span data-ttu-id="7bf10-116">Un valor de **tipo String** que contiene una dirección URL que especifica la ubicación donde se va a copiar *Source* .</span><span class="sxs-lookup"><span data-stu-id="7bf10-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="7bf10-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="7bf10-117">*UserName*</span></span> |<span data-ttu-id="7bf10-p103">Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.</span><span class="sxs-lookup"><span data-stu-id="7bf10-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="7bf10-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="7bf10-120">*Password*</span></span> |<span data-ttu-id="7bf10-p104">Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.</span><span class="sxs-lookup"><span data-stu-id="7bf10-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="7bf10-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="7bf10-123">*Options*</span></span> |<span data-ttu-id="7bf10-p105">Es opcional. Valor de [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tiene **adCopyUnspecified** como valor predeterminado. Especifica el comportamiento de este método.</span><span class="sxs-lookup"><span data-stu-id="7bf10-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="7bf10-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="7bf10-127">*Async*</span></span> |<span data-ttu-id="7bf10-p106">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7bf10-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="7bf10-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bf10-130">Return value</span></span>

<span data-ttu-id="7bf10-p107">Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7bf10-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf10-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bf10-133">Remarks</span></span>

<span data-ttu-id="7bf10-134">Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7bf10-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="7bf10-135">Al menos uno de los nombres de servidor, ruta de acceso o recurso debe ser diferente.</span><span class="sxs-lookup"><span data-stu-id="7bf10-135">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="7bf10-p109">Todos los elementos secundarios de *Source* (por ejemplo, subdirectorios) se copian de forma recursiva, a menos que se especifique **adCopyNonRecursive**. En una operación recursiva, *Destination* no puede ser un subdirectorio de *Source*; en caso contrario, la operación no finalizará.</span><span class="sxs-lookup"><span data-stu-id="7bf10-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="7bf10-138">Este método se produce un error si *Destination* identifica una entidad existente (por ejemplo, un archivo o directorio), a menos que **se especifique adCopyOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="7bf10-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bf10-139">[!IMPORTANTE] Utilice la opción **adCopyOverWrite** con criterio.</span><span class="sxs-lookup"><span data-stu-id="7bf10-139">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="7bf10-140">Por ejemplo, si especifica esta opción cuando copia un archivo en un directorio va a *Eliminar* el directorio y reemplácelo con el archivo.</span><span class="sxs-lookup"><span data-stu-id="7bf10-140">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="7bf10-141">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="7bf10-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="7bf10-142">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="7bf10-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


