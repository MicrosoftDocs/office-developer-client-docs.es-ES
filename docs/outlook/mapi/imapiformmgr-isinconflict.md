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
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="0aff2-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="0aff2-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="0aff2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aff2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aff2-105">Determina si un formulario puede controlar sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0aff2-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="0aff2-106">Un mensaje está en conflicto si ha sido editado simultáneamente por más de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0aff2-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="0aff2-107">Esto puede ocurrir con mensajes en carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="0aff2-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="0aff2-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="0aff2-108">Parameters</span></span>

 <span data-ttu-id="0aff2-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="0aff2-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="0aff2-110">a Un puntero a una máscara de máscara de marcas copiada de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de un mensaje que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0aff2-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="0aff2-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="0aff2-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="0aff2-112">a Una máscara de bits de marcadores definidos por el cliente o definidos por el proveedor que se copian de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de un mensaje que proporciona información adicional sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0aff2-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="0aff2-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="0aff2-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="0aff2-114">a Una cadena que asigna un nombre A la clase de mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0aff2-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="0aff2-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="0aff2-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="0aff2-116">a Un puntero a la carpeta que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0aff2-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="0aff2-117">El parámetro _pFolderFocus_ puede ser null si no existe una carpeta de este tipo (por ejemplo, si el mensaje está incrustado en otro mensaje).</span><span class="sxs-lookup"><span data-stu-id="0aff2-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0aff2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aff2-118">Return value</span></span>

<span data-ttu-id="0aff2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aff2-119">S_OK</span></span> 
  
> <span data-ttu-id="0aff2-120">El formulario no controla sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0aff2-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="0aff2-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="0aff2-121">S_FALSE</span></span> 
  
> <span data-ttu-id="0aff2-122">El formulario administra sus propios conflictos de mensajes o el mensaje para el que se pasó la información no está en conflicto.</span><span class="sxs-lookup"><span data-stu-id="0aff2-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aff2-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0aff2-123">Remarks</span></span>

<span data-ttu-id="0aff2-124">Los visores de formularios llaman al método **IMAPIFormMgr:: IsInConflict** para descubrir si un formulario en particular no controla sus propios conflictos de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0aff2-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="0aff2-125">**IsInConflict** comprueba la máscaras de de los parámetros _ulMessageFlags_ y _ulMessageStatus_ para la presencia de una marca de conflicto.</span><span class="sxs-lookup"><span data-stu-id="0aff2-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="0aff2-126">Si se establece una marca de conflicto, **IsInConflict** resuelve la clase de mensaje pasada en el parámetro _SZMESSAGECLASS_ y Devuelve S_OK si el formulario no controla sus propios conflictos.</span><span class="sxs-lookup"><span data-stu-id="0aff2-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="0aff2-127">**IsInConflict** devuelve S_FALSE si el formulario controla sus propios conflictos.</span><span class="sxs-lookup"><span data-stu-id="0aff2-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="0aff2-128">Un formulario que no controla sus propios conflictos se debe abrir mediante el método [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) y no puede volver a usar un objeto Form existente.</span><span class="sxs-lookup"><span data-stu-id="0aff2-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0aff2-129">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0aff2-129">Notes to callers</span></span>

<span data-ttu-id="0aff2-130">Las aplicaciones cliente suelen tener que enfrentarse a conflictos cuando las aplicaciones se mueven de un mensaje al mensaje siguiente o anterior de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0aff2-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="0aff2-131">Si un mensaje está en conflicto, pero el servidor de formularios para ese mensaje puede controlar conflictos, la aplicación cliente debe ejecutar su código habitual para mostrar el mensaje siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="0aff2-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="0aff2-132">Si el servidor de formularios no puede controlar conflictos, la aplicación cliente debe continuar como si no hubiera constancia de la clase de mensaje del mensaje siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="0aff2-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0aff2-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="0aff2-133">See also</span></span>



[<span data-ttu-id="0aff2-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="0aff2-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="0aff2-135">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="0aff2-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="0aff2-136">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0aff2-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="0aff2-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aff2-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

