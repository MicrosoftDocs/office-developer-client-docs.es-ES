---
title: DeleteRecord (método, ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483514"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="0f7b4-102">DeleteRecord (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="0f7b4-102">DeleteRecord Method (ADO)</span></span>


<span data-ttu-id="0f7b4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f7b4-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="0f7b4-104">Elimina la entidad representada por un objeto [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0f7b4-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f7b4-105">Syntax</span></span>

<span data-ttu-id="0f7b4-106">*Registro*. \**DeleteRecord \*\*\* origen*, *Async*</span><span class="sxs-lookup"><span data-stu-id="0f7b4-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="0f7b4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f7b4-107">Parameters</span></span>

  - <span data-ttu-id="0f7b4-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="0f7b4-108">*Source*</span></span>

  - <span data-ttu-id="0f7b4-p101">Es opcional. Valor de tipo **String** con una dirección URL que identifica la entidad (por ejemplo, un archivo o directorio) que se va a eliminar. Si se omite *Source* o se especifica una cadena vacía, se elimina la entidad representada por el actual objeto [Record](record-object-ado.md). Si el objeto Record es un registro de colección (el valor de [RecordType](recordtype-property-ado.md) es **adCollectionRecord**, como un directorio), también se eliminarán todos los objetos secundarios (por ejemplo, subdirectorios).</span><span class="sxs-lookup"><span data-stu-id="0f7b4-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="0f7b4-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="0f7b4-113">*Async*</span></span>

  - <span data-ttu-id="0f7b4-p102">Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que la operación de eliminación es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7b4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0f7b4-116">Remarks</span></span>

<span data-ttu-id="0f7b4-p103">Puede que las operaciones que se realicen en el objeto representado por este objeto **Record** generen un error después de finalizar este método. Tras llamar a **DeleteRecord**, el objeto **Record** debe estar cerrado porque el comportamiento del objeto **Record** puede volverse impredecible, dependiendo del momento en que el proveedor actualice el objeto **Record** con el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="0f7b4-119">Si este objeto **Record** se obtuvo de un objeto [Recordset](recordset-object-ado.md), los resultados de esta operación no se reflejarán inmediatamente en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="0f7b4-120">Actualizar el **conjunto de registros** , cierre y vuelva a abrirlo, o mediante la ejecución de los métodos de **Recordset** [Requery](requery-method-ado.md), o [Update](update-method-ado.md) y [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0f7b4-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0f7b4-p105">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="0f7b4-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


