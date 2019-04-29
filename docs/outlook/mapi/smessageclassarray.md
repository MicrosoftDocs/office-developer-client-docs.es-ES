---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412698"
---
# <a name="smessageclassarray"></a><span data-ttu-id="01499-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="01499-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="01499-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01499-105">Contiene una matriz de punteros a cadenas de clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="01499-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01499-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="01499-106">Header file:</span></span>  <br/> |<span data-ttu-id="01499-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="01499-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="01499-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="01499-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="01499-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="01499-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="01499-110">Members</span><span class="sxs-lookup"><span data-stu-id="01499-110">Members</span></span>

 <span data-ttu-id="01499-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="01499-111">**cValues**</span></span>
  
> <span data-ttu-id="01499-112">Número de punteros de cadena de clase de mensaje en la matriz.</span><span class="sxs-lookup"><span data-stu-id="01499-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="01499-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="01499-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="01499-114">Matriz de punteros a cadenas de clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="01499-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01499-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="01499-115">Remarks</span></span>

<span data-ttu-id="01499-116">La estructura **SMessageClassArray** se pasa como un parámetro en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="01499-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="01499-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="01499-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="01499-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="01499-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="01499-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="01499-119">See also</span></span>



[<span data-ttu-id="01499-120">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="01499-120">MAPI Structures</span></span>](mapi-structures.md)

