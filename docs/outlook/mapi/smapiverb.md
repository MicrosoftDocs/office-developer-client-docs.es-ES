---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 11f11ae2d90a951a119895f3e0e3e3ca0dbc0fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573701"
---
# <a name="smapiverb"></a><span data-ttu-id="597bc-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="597bc-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="597bc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="597bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="597bc-105">Describe un verbo MAPI.</span><span class="sxs-lookup"><span data-stu-id="597bc-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="597bc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="597bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="597bc-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="597bc-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="597bc-108">Members</span><span class="sxs-lookup"><span data-stu-id="597bc-108">Members</span></span>

 <span data-ttu-id="597bc-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="597bc-109">**lVerb**</span></span>
  
> <span data-ttu-id="597bc-110">Código que representa el verbo que se pasa a [IMAPIForm::DoVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="597bc-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="597bc-111">Los verbos estándar se definen en el archivo de encabezado Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="597bc-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="597bc-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="597bc-112">**szVerbname**</span></span>
  
> <span data-ttu-id="597bc-113">Nombre para mostrar del verbo tal como aparece en el menú formulario.</span><span class="sxs-lookup"><span data-stu-id="597bc-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="597bc-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="597bc-114">**fuFlags**</span></span>
  
> <span data-ttu-id="597bc-115">Marcas para el verbo.</span><span class="sxs-lookup"><span data-stu-id="597bc-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="597bc-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="597bc-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="597bc-117">Atributos del verbo.</span><span class="sxs-lookup"><span data-stu-id="597bc-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="597bc-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="597bc-118">**ulFlags**</span></span>
  
> <span data-ttu-id="597bc-119">Marca que indica el formato de nombre para mostrar del verbo.</span><span class="sxs-lookup"><span data-stu-id="597bc-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="597bc-120">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="597bc-120">The following flag can be set:</span></span>
    
<span data-ttu-id="597bc-121">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="597bc-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="597bc-122">Es el nombre para mostrar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="597bc-122">The display name is in Unicode format.</span></span> <span data-ttu-id="597bc-123">Si no está establecido el indicador MAPI_UNICODE., el nombre para mostrar está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="597bc-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="597bc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="597bc-124">Remarks</span></span>

<span data-ttu-id="597bc-125">La estructura **SMAPIVerb** se pasa como un parámetro en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="597bc-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="597bc-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="597bc-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="597bc-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="597bc-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="597bc-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="597bc-128">See also</span></span>



[<span data-ttu-id="597bc-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="597bc-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="597bc-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="597bc-130">MAPI Structures</span></span>](mapi-structures.md)

