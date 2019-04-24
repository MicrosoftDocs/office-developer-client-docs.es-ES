---
title: SaveToFile (método, ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308928"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="d9a38-102">SaveToFile (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="d9a38-102">SaveToFile method (ADO)</span></span>

<span data-ttu-id="d9a38-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9a38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9a38-104">Guarda el contenido binario de un objeto [Stream](stream-object-ado.md) en un archivo.</span><span class="sxs-lookup"><span data-stu-id="d9a38-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9a38-105">Syntax</span></span>

<span data-ttu-id="d9a38-106">*Secuencia*. *Nombre de archivo*de SaveToFile, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="d9a38-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="d9a38-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9a38-107">Parameters</span></span>

|<span data-ttu-id="d9a38-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9a38-108">Parameter</span></span>|<span data-ttu-id="d9a38-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9a38-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d9a38-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d9a38-110">*FileName*</span></span> |<span data-ttu-id="d9a38-p101">Valor de tipo **String** que contiene el nombre completo del archivo en el que se va a guardar el contenido del objeto **Stream**. Se puede guardar en cualquier ubicación local válida o cualquier ubicación a la que se tenga acceso mediante un valor UNC.</span><span class="sxs-lookup"><span data-stu-id="d9a38-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>|
|<span data-ttu-id="d9a38-113">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="d9a38-113">*SaveOptions*</span></span> |<span data-ttu-id="d9a38-p102">Valor de [SaveOptionsEnum](saveoptionsenum.md) que especifica si **SaveToFile** debe crear un archivo nuevo si aún no existe. El valor predeterminado es **adSaveCreateNotExists**. Con estas opciones, se puede especificar que se genere un error si no existe el archivo indicado. Asimismo, se puede especificar que **SaveToFile** sobrescriba el contenido de un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="d9a38-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>|

> [!NOTE]
> <span data-ttu-id="d9a38-118">Si se sobrescribe un archivo existente (cuando se ha establecido el valor **adSaveCreateOverwrite**), **SaveToFile** truncará los bytes del archivo existente original que aparezcan después del nuevo [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d9a38-118">If you overwrite an existing file (when **adSaveCreateOverwrite** is set), **SaveToFile** truncates any bytes from the original existing file that follow the new [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a38-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9a38-119">Remarks</span></span>

<span data-ttu-id="d9a38-p103">**SaveToFile** puede utilizarse para copiar el contenido de un objeto **Stream** en un archivo local. No se produce ningún cambio en el contenido ni en las propiedades del objeto **Stream**. El objeto **Stream** debe estar abierto antes de que se llame a **SaveToFile**.</span><span class="sxs-lookup"><span data-stu-id="d9a38-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="d9a38-p104">Este método no cambia la asociación del objeto **Stream** a su origen subyacente. El objeto **Stream** permanecerá asociado a la dirección URL original o al objeto **Record** que era su origen al abrirse.</span><span class="sxs-lookup"><span data-stu-id="d9a38-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="d9a38-125">Después de una operación de **SaveToFile**, la posición actual ([Position](position-property-ado.md)) en la secuencia se establece en el principio de la secuencia (0).</span><span class="sxs-lookup"><span data-stu-id="d9a38-125">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

