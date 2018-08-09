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
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820730"
---
# <a name="smapiverb"></a><span data-ttu-id="aa6b5-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="aa6b5-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="aa6b5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa6b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa6b5-105">Describe un verbo MAPI.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa6b5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="aa6b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa6b5-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="aa6b5-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="aa6b5-108">Members</span><span class="sxs-lookup"><span data-stu-id="aa6b5-108">Members</span></span>

 <span data-ttu-id="aa6b5-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-109">**lVerb**</span></span>
  
> <span data-ttu-id="aa6b5-110">Código que representa el verbo que se pasa a [IMAPIForm::DoVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="aa6b5-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="aa6b5-111">Los verbos estándar se definen en el archivo de encabezado Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="aa6b5-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-112">**szVerbname**</span></span>
  
> <span data-ttu-id="aa6b5-113">Nombre para mostrar del verbo tal como aparece en el menú formulario.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="aa6b5-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-114">**fuFlags**</span></span>
  
> <span data-ttu-id="aa6b5-115">Marcas para el verbo.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="aa6b5-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="aa6b5-117">Atributos del verbo.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="aa6b5-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="aa6b5-118">**ulFlags**</span></span>
  
> <span data-ttu-id="aa6b5-119">Marca que indica el formato de nombre para mostrar del verbo.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="aa6b5-120">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="aa6b5-120">The following flag can be set:</span></span>
    
<span data-ttu-id="aa6b5-121">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aa6b5-122">Es el nombre para mostrar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-122">The display name is in Unicode format.</span></span> <span data-ttu-id="aa6b5-123">Si no está establecido el indicador MAPI_UNICODE., el nombre para mostrar está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="aa6b5-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa6b5-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa6b5-124">Remarks</span></span>

<span data-ttu-id="aa6b5-125">La estructura **SMAPIVerb** se pasa como un parámetro en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="aa6b5-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="aa6b5-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="aa6b5-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="aa6b5-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="aa6b5-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="aa6b5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa6b5-128">See also</span></span>



[<span data-ttu-id="aa6b5-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="aa6b5-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="aa6b5-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="aa6b5-130">MAPI Structures</span></span>](mapi-structures.md)

