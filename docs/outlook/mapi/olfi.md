---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279756"
---
# <a name="olfi"></a><span data-ttu-id="420df-103">OLFI</span><span class="sxs-lookup"><span data-stu-id="420df-103">OLFI</span></span>

  
  
<span data-ttu-id="420df-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="420df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="420df-105">Cola de estructuras de identificador a largo plazo usadas por el proveedor de almacén de archivos de carpetas personales (PST) para asignar un identificador de entrada para un mensaje o una carpeta nuevos en el modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="420df-105">Queue of long-term ID structures used by the Personal Folders file (PST) store provider to assign an Entry ID for a new message or folder in offline mode.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="420df-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="420df-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a><span data-ttu-id="420df-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="420df-107">Members</span></span>

 <span data-ttu-id="420df-108">_ulVersion_</span><span class="sxs-lookup"><span data-stu-id="420df-108">_ulVersion_</span></span>
  
- <span data-ttu-id="420df-109">Número de versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="420df-109">Version number for the structure.</span></span> 
    
 <span data-ttu-id="420df-110">_muidReserved_</span><span class="sxs-lookup"><span data-stu-id="420df-110">_muidReserved_</span></span>
  
- <span data-ttu-id="420df-111">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="420df-111">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="420df-112">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="420df-112">_ulReserved_</span></span>
  
- <span data-ttu-id="420df-113">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="420df-113">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="420df-114">_dwAlloc_</span><span class="sxs-lookup"><span data-stu-id="420df-114">_dwAlloc_</span></span>
  
- <span data-ttu-id="420df-115">Número de entradas que están disponibles para la asignación.</span><span class="sxs-lookup"><span data-stu-id="420df-115">The number of entries that are available for allocation.</span></span> <span data-ttu-id="420df-116">Estas entradas comparten el mismo identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="420df-116">These entries share the same globally unique identifier (GUID).</span></span>
    
 <span data-ttu-id="420df-117">_dwNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="420df-117">_dwNextAlloc_</span></span>
  
- <span data-ttu-id="420df-118">Número de entradas disponibles a continuación para la asignación.</span><span class="sxs-lookup"><span data-stu-id="420df-118">The number of entries that are available next for allocation.</span></span> <span data-ttu-id="420df-119">Estas entradas comparten el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="420df-119">These entries share the same GUID.</span></span>
    
 <span data-ttu-id="420df-120">_ltidAlloc_</span><span class="sxs-lookup"><span data-stu-id="420df-120">_ltidAlloc_</span></span>
  
- <span data-ttu-id="420df-121">La estructura del identificador a largo plazo, **[LTID](ltid.md)**, que identifica la entrada actualmente disponible para la asignación.</span><span class="sxs-lookup"><span data-stu-id="420df-121">The long-term ID structure, **[LTID](ltid.md)**, identifying the entry currently available for allocation.</span></span> <span data-ttu-id="420df-122">La estructura de identificador a largo plazo contiene un GUID y un índice que identifica un objeto en el almacén.</span><span class="sxs-lookup"><span data-stu-id="420df-122">The long-term ID structure contains a GUID and an index identifying an object in the store.</span></span> <span data-ttu-id="420df-123">Juntos, el GUID y el índice pueden formar un identificador de entrada único para un objeto.</span><span class="sxs-lookup"><span data-stu-id="420df-123">Together, the GUID and the index can form a unique Entry ID for an object.</span></span> 
    
 <span data-ttu-id="420df-124">_ltidNextAlloc_</span><span class="sxs-lookup"><span data-stu-id="420df-124">_ltidNextAlloc_</span></span>
  
- <span data-ttu-id="420df-125">Estructura de identificador a largo plazo que identifica la siguiente entrada disponible.</span><span class="sxs-lookup"><span data-stu-id="420df-125">Long-term ID structure identifying the next available entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="420df-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="420df-126">Remarks</span></span>

<span data-ttu-id="420df-127">Un identificador de entrada es un identificador de entrada MAPI de 4 bytes para una carpeta o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="420df-127">An Entry ID is a 4-byte MAPI entry identifier for a folder or a message.</span></span> <span data-ttu-id="420df-128">Para obtener más información, vea [EntryID](https://msdn.microsoft.com/library/ms836424).</span><span class="sxs-lookup"><span data-stu-id="420df-128">For more information, see [ENTRYID](https://msdn.microsoft.com/library/ms836424).</span></span>
  
<span data-ttu-id="420df-129">Cuando un proveedor de almacén de PST asigna un identificador de entrada a un nuevo objeto, primero necesita un GUID que identifique el servidor y un índice que identifica el objeto en el almacén.</span><span class="sxs-lookup"><span data-stu-id="420df-129">When a PST store provider assigns an Entry ID to a new object, it first needs a GUID that identifies the server, and an index that identifies the object in the store.</span></span> <span data-ttu-id="420df-130">Aunque el GUID no es único en todos los identificadores de entrada, el GUID y el índice combinados proporcionan una única entrada.</span><span class="sxs-lookup"><span data-stu-id="420df-130">Even though the GUID is not unique across all Entry IDs, the GUID and the index combined provide a unique entry.</span></span> <span data-ttu-id="420df-131">Una estructura de identificador a largo plazo tiene un seguimiento del GUID y el par de índice, **LTID**, que forma parte de la estructura **OLFI** .</span><span class="sxs-lookup"><span data-stu-id="420df-131">This GUID and index pair is tracked by a long-term ID structure, **LTID**, which is part of the **OLFI** structure.</span></span> 
  
<span data-ttu-id="420df-132">El proveedor de almacén de archivos PST no mantiene físicamente **OLFI** una estructura de **LTID** para cada par de GUID-índice.</span><span class="sxs-lookup"><span data-stu-id="420df-132">The PST store provider does not physically keep in **OLFI** an **LTID** structure for each GUID-index pair.</span></span> <span data-ttu-id="420df-133">Mantiene una estructura **LTID** , *ltidAlloc* , para el primer par GUID disponible actualmente; un recuento, *dwAlloc* , del número de entradas disponibles que comparten el mismo GUID; y una segunda estructura **LTID** , *ltidNextAlloc* , para el siguiente par GUID-índice disponible que tiene un GUID diferente.</span><span class="sxs-lookup"><span data-stu-id="420df-133">It keeps one **LTID** structure,  *ltidAlloc*  , for the currently first available GUID-index pair; a count,  *dwAlloc*  , of the number of available entries that share this same GUID; and a second **LTID** structure,  *ltidNextAlloc*  , for the next available GUID-index pair that has a different GUID.</span></span> <span data-ttu-id="420df-134">El proveedor de almacén de PST usa la estructura **OLFI** para realizar un seguimiento de los GUID e índices que ha distribuido. En un nivel virtual, el proveedor mantiene una reserva de varias estructuras **LTID** que están listas para ser asignadas.</span><span class="sxs-lookup"><span data-stu-id="420df-134">The PST store provider uses the **OLFI** structure to track the GUIDs and indexes that it has handed out. At a virtual level, the provider maintains a reserve of a number of **LTID** structures that are ready to be allocated.</span></span>  <span data-ttu-id="420df-135">*dwAlloc* mantiene un recuento de las estructuras de **LTID** disponibles.</span><span class="sxs-lookup"><span data-stu-id="420df-135">*dwAlloc*  maintains a count of the available **LTID** structures.</span></span> 
  
<span data-ttu-id="420df-136">Las solicitudes de identificadores de entrada se incluyen en bloques.</span><span class="sxs-lookup"><span data-stu-id="420df-136">Requests for Entry IDs come in blocks.</span></span> <span data-ttu-id="420df-137">Cuando hay una solicitud para un bloque, el proveedor del almacén de PST comprueba si hay suficiente reserva disponible comparando el tamaño solicitado con *dwAlloc* .</span><span class="sxs-lookup"><span data-stu-id="420df-137">When there is a request for a block, the PST store provider checks if there is sufficient reserve on hand by comparing the requested size with  *dwAlloc*  .</span></span> <span data-ttu-id="420df-138">Si hay suficiente Reserve, devuelve el GUID y el índice en *ltidAlloc* para la asignación.</span><span class="sxs-lookup"><span data-stu-id="420df-138">If there is sufficient reserve, it returns the GUID and index in  *ltidAlloc*  for allocation.</span></span> <span data-ttu-id="420df-139">A continuación, se reduce la *dwAlloc* del tamaño solicitado y se incrementa el índice en *ltidAlloc* por el tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="420df-139">It then decreases  *dwAlloc*  by the requested size, and increments the index in  *ltidAlloc*  by the requested size.</span></span> <span data-ttu-id="420df-140">Esto prepara el proveedor de almacén PST para asignar *ltidAlloc* en la siguiente solicitud para otro bloque de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="420df-140">This prepares the PST store provider to allocate  *ltidAlloc*  on the next request for another block of Entry IDs.</span></span> <span data-ttu-id="420df-141">Tenga en cuenta que el GUID sigue siendo el mismo para la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="420df-141">Note that the GUID remains the same for the next request.</span></span> 
  
<span data-ttu-id="420df-142">Si el tamaño de una solicitud es superior a *dwAlloc* , el proveedor de almacén de archivos PST intenta usar lo que tiene junto en Reserve, según se especifica en *dwNextAlloc* y *ltidNextAlloc* .</span><span class="sxs-lookup"><span data-stu-id="420df-142">If the size of a request is larger than  *dwAlloc*  , the PST store provider tries to use what it has next in reserve, as specified by  *dwNextAlloc*  and  *ltidNextAlloc*  .</span></span> <span data-ttu-id="420df-143">Copia *dwNextAlloc* y *ltidNextAlloc* a *dwAlloc* y *LtidAlloc* respectivamente, y establece *dwNextAlloc* y *ltidNextAlloc* en NULL.</span><span class="sxs-lookup"><span data-stu-id="420df-143">It copies  *dwNextAlloc*  and  *ltidNextAlloc*  to  *dwAlloc*  and  *ltidAlloc*  respectively, and sets  *dwNextAlloc*  and  *ltidNextAlloc*  to NULL.</span></span> 
  
<span data-ttu-id="420df-144">Un proveedor que envuelve al proveedor del almacén de PST debe comprobar periódicamente *ltidNextAlloc* para ver si es NULL.</span><span class="sxs-lookup"><span data-stu-id="420df-144">A provider that wraps the PST store provider should periodically check  *ltidNextAlloc*  to see if it is NULL.</span></span> <span data-ttu-id="420df-145">Si lo es, el proveedor debe rellenarlo con un nuevo GUID y restablecer *dwNextAlloc* para que se puedan asignar más identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="420df-145">If it is, the provider should populate it with a new GUID and reset  *dwNextAlloc*  so that more entry IDs can be allocated.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="420df-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="420df-146">See also</span></span>



[<span data-ttu-id="420df-147">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="420df-147">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="420df-148">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="420df-148">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="420df-149">LTID</span><span class="sxs-lookup"><span data-stu-id="420df-149">LTID</span></span>](ltid.md)

