---
title: LoadFromFile (método, ADO)
TOCTitle: LoadFromFile Method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a2a86e739b8744f40c481eb81b86f2f1ae5fad12
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483543"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="89cb3-102">LoadFromFile (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="89cb3-102">LoadFromFile Method (ADO)</span></span>


<span data-ttu-id="89cb3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89cb3-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="89cb3-104">Carga el contenido de un archivo existente en un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="89cb3-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="89cb3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89cb3-105">Syntax</span></span>

<span data-ttu-id="89cb3-106">*Secuencia*. LoadFromFile *FileName*</span><span class="sxs-lookup"><span data-stu-id="89cb3-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameter"></a><span data-ttu-id="89cb3-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="89cb3-107">Parameter</span></span>

  - <span data-ttu-id="89cb3-108">*FileName*</span><span class="sxs-lookup"><span data-stu-id="89cb3-108">*FileName*</span></span>

  - <span data-ttu-id="89cb3-109">Valor de tipo **String** que contiene el nombre del archivo que se va a cargar en el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="89cb3-109">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="89cb3-110">*Nombre de archivo* puede contener cualquier ruta de acceso válida y un nombre en formato UNC.</span><span class="sxs-lookup"><span data-stu-id="89cb3-110">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="89cb3-111">Si no existe el archivo especificado, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="89cb3-111">If the specified file does not exist, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="89cb3-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89cb3-112">Remarks</span></span>

<span data-ttu-id="89cb3-p102">Este método se puede utilizar para cargar el contenido de un archivo local en un objeto **Stream**; por ejemplo, para cargar el contenido de un archivo local en un servidor.</span><span class="sxs-lookup"><span data-stu-id="89cb3-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="89cb3-p103">El objeto **Stream** ya debe estar abierto antes de que se llame a **LoadFromFile**. Este método no cambia el enlace del objeto **Stream**; seguirá enlazado al objeto especificado por la dirección URL o el objeto **Record** con el que se abrió originalmente el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="89cb3-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="89cb3-p104">**LoadFromFile** sobrescribe el contenido actual del objeto **Stream** con los datos del archivo que se leen. Los bytes existentes en el objeto **Stream** se sobrescriben con el contenido del archivo. Se truncan los bytes que existían anteriormente o que permanecen después de [EOS](eos-property-ado.md) que crea **LoadFromFile**.</span><span class="sxs-lookup"><span data-stu-id="89cb3-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="89cb3-120">Tras llamar a **LoadFromFile**, la posición actual se establece en el principio del objeto **Stream** (el valor de [Position](position-property-ado.md) es 0).</span><span class="sxs-lookup"><span data-stu-id="89cb3-120">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="89cb3-121">Dado que se pueden agregar 2 bytes al principio de la secuencia para la codificación, puede que el tamaño de la secuencia no coincida exactamente con el tamaño del archivo desde el cual se cargó.</span><span class="sxs-lookup"><span data-stu-id="89cb3-121">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

