---
title: SaveToFile (método, ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0bd915a4eb6405b7d5ddd4bfe42eb4a98f68b89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483940"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="50f7c-102">SaveToFile (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="50f7c-102">SaveToFile Method (ADO)</span></span>


<span data-ttu-id="50f7c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="50f7c-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="50f7c-104">Guarda el contenido binario de un objeto [Stream](stream-object-ado.md) en un archivo.</span><span class="sxs-lookup"><span data-stu-id="50f7c-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50f7c-105">Syntax</span></span>

<span data-ttu-id="50f7c-106">*Secuencia*. SaveToFile*FileName*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="50f7c-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="50f7c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50f7c-107">Parameters</span></span>

  - <span data-ttu-id="50f7c-108">*FileName*</span><span class="sxs-lookup"><span data-stu-id="50f7c-108">*FileName*</span></span>

  - <span data-ttu-id="50f7c-p101">Valor de tipo **String** que contiene el nombre completo del archivo en el que se va a guardar el contenido del objeto **Stream**. Se puede guardar en cualquier ubicación local válida o cualquier ubicación a la que se tenga acceso mediante un valor UNC.</span><span class="sxs-lookup"><span data-stu-id="50f7c-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>

  - <span data-ttu-id="50f7c-111">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="50f7c-111">*SaveOptions*</span></span>

  - <span data-ttu-id="50f7c-p102">Valor de [SaveOptionsEnum](saveoptionsenum.md) que especifica si **SaveToFile** debe crear un archivo nuevo si aún no existe. El valor predeterminado es **adSaveCreateNotExists**. Con estas opciones, se puede especificar que se genere un error si no existe el archivo indicado. Asimismo, se puede especificar que **SaveToFile** sobrescriba el contenido de un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="50f7c-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>


> [!NOTE]
> <P><span data-ttu-id="50f7c-116">[!NOTA] Si se sobrescribe un archivo existente (cuando se ha establecido el valor <STRONG>adSaveCreateOverwrite</STRONG> ), <STRONG>SaveToFile</STRONG> truncará los bytes del archivo existente original que aparezcan después del nuevo <A href="eos-property-ado.md">EOS</A>.</span><span class="sxs-lookup"><span data-stu-id="50f7c-116">If you overwrite an existing file (when <STRONG>adSaveCreateOverwrite</STRONG> is set), <STRONG>SaveToFile</STRONG> truncates any bytes from the original existing file that follow the new <A href="eos-property-ado.md">EOS</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="50f7c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50f7c-117">Remarks</span></span>

<span data-ttu-id="50f7c-p103">**SaveToFile** puede utilizarse para copiar el contenido de un objeto **Stream** en un archivo local. No se produce ningún cambio en el contenido ni en las propiedades del objeto **Stream**. El objeto **Stream** debe estar abierto antes de que se llame a **SaveToFile**.</span><span class="sxs-lookup"><span data-stu-id="50f7c-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="50f7c-p104">Este método no cambia la asociación del objeto **Stream** a su origen subyacente. El objeto **Stream** permanecerá asociado a la dirección URL original o al objeto **Record** que era su origen al abrirse.</span><span class="sxs-lookup"><span data-stu-id="50f7c-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="50f7c-123">Después de una operación de **SaveToFile**, la posición actual ([Position](position-property-ado.md)) en la secuencia se establece en el principio de la secuencia (0).</span><span class="sxs-lookup"><span data-stu-id="50f7c-123">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>
