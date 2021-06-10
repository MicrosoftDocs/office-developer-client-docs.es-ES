---
title: Método CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295530"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="ce79d-102">Método CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="ce79d-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="ce79d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce79d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce79d-104">Copia una entidad representada por un objeto **Record** en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="ce79d-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce79d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce79d-105">Syntax</span></span>

<span data-ttu-id="ce79d-106">*Grabar*. CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="ce79d-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ce79d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce79d-107">Parameters</span></span>

|<span data-ttu-id="ce79d-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ce79d-108">Parameter</span></span>|<span data-ttu-id="ce79d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce79d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ce79d-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="ce79d-110">*Source*</span></span> |<span data-ttu-id="ce79d-p101">Es opcional. Valor de tipo **String** con la dirección URL que especifica la entidad que se va a copiar (por ejemplo, un archivo o directorio). Si se omite *Source* o especifica una cadena vacía, se copiará el archivo o directorio representado por el actual objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ce79d-p101">Optional. A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory). If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="ce79d-114">*Destino*</span><span class="sxs-lookup"><span data-stu-id="ce79d-114">*Destination*</span></span> |<span data-ttu-id="ce79d-p102">Es opcional. Valor de tipo **String** con la dirección URL que especifica la ubicación en la que se va a copiar *Source*.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p102">Optional. A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="ce79d-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="ce79d-117">*UserName*</span></span> |<span data-ttu-id="ce79d-p103">Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="ce79d-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="ce79d-120">*Password*</span></span> |<span data-ttu-id="ce79d-p104">Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="ce79d-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="ce79d-123">*Options*</span></span> |<span data-ttu-id="ce79d-p105">Es opcional. Valor de [CopyRecordOptionsEnum](copyrecordoptionsenum.md) que tiene **adCopyUnspecified** como valor predeterminado. Especifica el comportamiento de este método.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="ce79d-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="ce79d-127">*Async*</span></span> |<span data-ttu-id="ce79d-p106">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que esta operación debe ser asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="ce79d-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce79d-130">Return value</span></span>

<span data-ttu-id="ce79d-p107">Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce79d-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce79d-133">Remarks</span></span>

<span data-ttu-id="ce79d-p108">Los valores de *Source* y *Destination* no pueden ser idénticos; en caso contrario, se produce un error en tiempo de ejecución. Al menos uno de los nombres de servidor, ruta de acceso o recurso debe ser diferente.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="ce79d-p109">Todos los elementos secundarios de *Source* (por ejemplo, subdirectorios) se copian de forma recursiva, a menos que se especifique **adCopyNonRecursive**. En una operación recursiva, *Destination* no puede ser un subdirectorio de *Source*; en caso contrario, la operación no finalizará.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="ce79d-138">Este método genera un error si *Destination* identifica una entidad existente (por ejemplo, un archivo o directorio), a menos que se especifique **adCopyOverWrite**.</span><span class="sxs-lookup"><span data-stu-id="ce79d-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce79d-p110">Utilice la opción **adCopyOverWrite** con criterio. Por ejemplo, si especifica esta opción cuando copia un archivo en un directorio, se *eliminará* el directorio y se reemplazará con el archivo.</span><span class="sxs-lookup"><span data-stu-id="ce79d-p110">Use the **adCopyOverWrite** option judiciously. For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="ce79d-141">[!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="ce79d-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ce79d-142">Para obtener más información, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="ce79d-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


