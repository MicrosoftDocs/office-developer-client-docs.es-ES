---
title: Método DeleteRecord (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293997"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="bde7d-102">Método DeleteRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="bde7d-102">DeleteRecord method (ADO)</span></span>

<span data-ttu-id="bde7d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bde7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bde7d-104">Elimina la entidad representada por un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bde7d-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bde7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bde7d-105">Syntax</span></span>

<span data-ttu-id="bde7d-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span><span class="sxs-lookup"><span data-stu-id="bde7d-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="bde7d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bde7d-107">Parameters</span></span>

|<span data-ttu-id="bde7d-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bde7d-108">Parameter</span></span>|<span data-ttu-id="bde7d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bde7d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bde7d-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="bde7d-110">*Source*</span></span> |<span data-ttu-id="bde7d-p101">Es opcional. Valor de tipo **String** con una dirección URL que identifica la entidad (por ejemplo, un archivo o directorio) que se va a eliminar. Si se omite *Source* o se especifica una cadena vacía, se elimina la entidad representada por el actual objeto [Record](record-object-ado.md). Si el objeto Record es un registro de colección (el valor de [RecordType](recordtype-property-ado.md) es **adCollectionRecord**, como un directorio), también se eliminarán todos los objetos secundarios (por ejemplo, subdirectorios).</span><span class="sxs-lookup"><span data-stu-id="bde7d-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>|
|<span data-ttu-id="bde7d-115">*Async*</span><span class="sxs-lookup"><span data-stu-id="bde7d-115">*Async*</span></span> |<span data-ttu-id="bde7d-p102">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que la operación de eliminación es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bde7d-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bde7d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bde7d-118">Remarks</span></span>

<span data-ttu-id="bde7d-p103">Puede que las operaciones que se realicen en el objeto representado por este objeto **Record** generen un error después de finalizar este método. Tras llamar a **DeleteRecord**, el objeto **Record** debe estar cerrado porque el comportamiento del objeto **Record** puede volverse impredecible, dependiendo del momento en que el proveedor actualice el objeto **Record** con el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="bde7d-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="bde7d-121">Si este objeto **Record** se obtuvo de un objeto [Recordset](recordset-object-ado.md), los resultados de esta operación no se reflejarán inmediatamente en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bde7d-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="bde7d-122">Actualice el **conjunto de** registros cerrando y abriendo de nuevo, o ejecutando los métodos **Recordset** [Requery](requery-method-ado.md)o [Update](update-method-ado.md) y [Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="bde7d-122">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>

> [!NOTE]
> <span data-ttu-id="bde7d-123">[!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="bde7d-123">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="bde7d-124">Para obtener más información, vea [Direcciones URL absolutas y relativas.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="bde7d-124">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


