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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 01563e3655d42abc62ea88a12f2878e5d81129d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820729"
---
# <a name="smessageclassarray"></a><span data-ttu-id="7f3c5-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="7f3c5-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="7f3c5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f3c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f3c5-105">Contiene una matriz de punteros a cadenas de clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7f3c5-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f3c5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7f3c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f3c5-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="7f3c5-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7f3c5-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="7f3c5-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7f3c5-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="7f3c5-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="7f3c5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f3c5-110">Members</span></span>

 <span data-ttu-id="7f3c5-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7f3c5-111">**cValues**</span></span>
  
> <span data-ttu-id="7f3c5-112">Recuento de punteros de cadena de clase de mensaje en la matriz.</span><span class="sxs-lookup"><span data-stu-id="7f3c5-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="7f3c5-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="7f3c5-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="7f3c5-114">Matriz de punteros a las cadenas de clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7f3c5-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f3c5-115">Notas</span><span class="sxs-lookup"><span data-stu-id="7f3c5-115">Remarks</span></span>

<span data-ttu-id="7f3c5-116">La estructura **SMessageClassArray** se pasa como un parámetro en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7f3c5-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="7f3c5-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7f3c5-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="7f3c5-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7f3c5-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="7f3c5-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="7f3c5-119">See also</span></span>



[<span data-ttu-id="7f3c5-120">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7f3c5-120">MAPI Structures</span></span>](mapi-structures.md)

