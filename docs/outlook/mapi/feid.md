---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Última modificación: 2012 de julio de 2002'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334842"
---
# <a name="feid"></a><span data-ttu-id="6524e-103">FEID</span><span class="sxs-lookup"><span data-stu-id="6524e-103">FEID</span></span>

 
  
<span data-ttu-id="6524e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6524e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6524e-105">Identificador de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="6524e-105">Identifier for a folder.</span></span> <span data-ttu-id="6524e-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="6524e-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6524e-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="6524e-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="6524e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6524e-108">Members</span></span>

 <span data-ttu-id="6524e-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="6524e-109">_abFlags_</span></span>
  
> <span data-ttu-id="6524e-110">identificador de entrada de 4 bytes para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6524e-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="6524e-111">Para obtener más información acerca de los identificadores de entrada MAPI, vea **[EntryID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="6524e-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="6524e-112">_Muid_</span><span class="sxs-lookup"><span data-stu-id="6524e-112">_muid_</span></span>
  
> <span data-ttu-id="6524e-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6524e-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="6524e-114">Consulte mapidefs. h para obtener la definición de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="6524e-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="6524e-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="6524e-115">_placeholder_</span></span>
  
> <span data-ttu-id="6524e-116">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="6524e-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="6524e-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="6524e-117">_ltid_</span></span>
  
> <span data-ttu-id="6524e-118">IDENTIFICADOR a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6524e-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6524e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6524e-119">See also</span></span>



[<span data-ttu-id="6524e-120">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="6524e-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="6524e-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6524e-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6524e-122">LTID</span><span class="sxs-lookup"><span data-stu-id="6524e-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="6524e-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="6524e-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="6524e-124">SINCRONIZÁNDOSE</span><span class="sxs-lookup"><span data-stu-id="6524e-124">SYNC</span></span>](sync.md)

