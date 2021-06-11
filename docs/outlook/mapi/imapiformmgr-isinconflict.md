---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412887"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="f1763-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="f1763-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="f1763-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1763-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1763-105">Determina si un formulario puede controlar sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f1763-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="f1763-106">Un mensaje está en conflicto si ha sido editado simultáneamente por más de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f1763-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="f1763-107">Esto puede suceder con los mensajes de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="f1763-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="f1763-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="f1763-108">Parameters</span></span>

 <span data-ttu-id="f1763-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="f1763-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="f1763-110">[in] Puntero a una máscara de bits de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de un mensaje que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f1763-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="f1763-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="f1763-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="f1763-112">[in] Máscara de bits de marcas definidas por el cliente o definidas por el proveedor copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de un mensaje que proporciona información adicional sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f1763-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="f1763-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="f1763-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="f1763-114">[in] Cadena que nombra la clase de mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f1763-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="f1763-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="f1763-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="f1763-116">[in] Puntero a la carpeta que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f1763-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="f1763-117">El  _parámetro pFolderFocus_ puede ser NULL si dicha carpeta no existe (por ejemplo, si el mensaje está incrustado en otro mensaje).</span><span class="sxs-lookup"><span data-stu-id="f1763-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f1763-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1763-118">Return value</span></span>

<span data-ttu-id="f1763-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1763-119">S_OK</span></span> 
  
> <span data-ttu-id="f1763-120">El formulario no controla sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f1763-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="f1763-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f1763-121">S_FALSE</span></span> 
  
> <span data-ttu-id="f1763-122">El formulario controla sus propios conflictos de mensajes o el mensaje para el que se ha pasado la información no está en conflicto.</span><span class="sxs-lookup"><span data-stu-id="f1763-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1763-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1763-123">Remarks</span></span>

<span data-ttu-id="f1763-124">Los visores de formularios llaman al método **IMAPIFormMgr::IsInConflict** para detectar si un formulario determinado no controla sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f1763-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="f1763-125">**IsInConflict comprueba** las máscaras de bits de los parámetros  _ulMessageFlags_ y  _ulMessageStatus_ en busca de la presencia de una marca de conflicto.</span><span class="sxs-lookup"><span data-stu-id="f1763-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="f1763-126">Si se establece una marca de conflicto, **IsInConflict** resuelve la clase de mensaje pasada en el  _parámetro szMessageClass_ y devuelve S_OK si el formulario no controla sus propios conflictos.</span><span class="sxs-lookup"><span data-stu-id="f1763-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="f1763-127">**IsInConflict** devuelve S_FALSE si el formulario controla sus propios conflictos.</span><span class="sxs-lookup"><span data-stu-id="f1763-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="f1763-128">Un formulario que no controla sus propios conflictos debe abrirse mediante el método [IMAPIFormMgr::LoadForm y](imapiformmgr-loadform.md) no puede volver a usar un objeto de formulario existente.</span><span class="sxs-lookup"><span data-stu-id="f1763-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1763-129">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="f1763-129">Notes to callers</span></span>

<span data-ttu-id="f1763-130">Las aplicaciones cliente suelen tener que lidiar con conflictos cuando las aplicaciones se mueven de un mensaje al siguiente o al mensaje anterior de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f1763-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="f1763-131">Si un mensaje está en conflicto, pero el servidor de formulario de ese mensaje puede controlar conflictos, la aplicación cliente debe ejecutar su código habitual para mostrar el mensaje siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="f1763-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="f1763-132">Si el servidor de formularios no puede controlar conflictos, la aplicación cliente debe continuar como si desconocía la clase de mensaje del mensaje siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="f1763-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1763-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1763-133">See also</span></span>



[<span data-ttu-id="f1763-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="f1763-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="f1763-135">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="f1763-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="f1763-136">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="f1763-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="f1763-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1763-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

