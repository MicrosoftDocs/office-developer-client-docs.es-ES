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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817304"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="ca444-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="ca444-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="ca444-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca444-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca444-105">Determina si un formulario puede controlar sus propio conflictos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="ca444-106">Un mensaje está en conflicto si se ha editado simultáneamente por más de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ca444-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="ca444-107">Esto puede ocurrir a los mensajes en las carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="ca444-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="ca444-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca444-108">Parameters</span></span>

 <span data-ttu-id="ca444-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="ca444-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="ca444-110">[entrada] Un puntero a una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de un mensaje que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="ca444-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="ca444-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="ca444-112">[entrada] Una máscara de bits de definidas por el cliente o definidas por el proveedor de indicadores que se copió desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de un mensaje que proporciona información adicional sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="ca444-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ca444-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="ca444-114">[entrada] Una cadena que da nombre de clase de mensaje del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="ca444-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="ca444-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="ca444-116">[entrada] Un puntero a la carpeta que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="ca444-117">El parámetro _pFolderFocus_ puede ser NULL si no existe como una carpeta (por ejemplo, si el mensaje está incrustado en otro mensaje).</span><span class="sxs-lookup"><span data-stu-id="ca444-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca444-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca444-118">Return value</span></span>

<span data-ttu-id="ca444-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca444-119">S_OK</span></span> 
  
> <span data-ttu-id="ca444-120">El formulario no controla sus propia conflictos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="ca444-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ca444-121">S_FALSE</span></span> 
  
> <span data-ttu-id="ca444-122">El formulario controla sus propio conflictos de mensaje o el mensaje para el que se pasó información no está en conflicto.</span><span class="sxs-lookup"><span data-stu-id="ca444-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca444-123">Notas</span><span class="sxs-lookup"><span data-stu-id="ca444-123">Remarks</span></span>

<span data-ttu-id="ca444-124">Visores de formulario llamar al método **IMAPIFormMgr::IsInConflict** para detectar si un formulario en particular no controla sus propia conflictos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca444-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="ca444-125">**IsInConflict** comprueba la máscara de bits en los parámetros _ulMessageFlags_ y _ulMessageStatus_ para la presencia de un indicador de conflicto.</span><span class="sxs-lookup"><span data-stu-id="ca444-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="ca444-126">Si se establece un indicador de conflicto, **IsInConflict** resuelve la clase de mensaje que se pasa en el parámetro _szMessageClass_ y devuelve S_OK si el formulario no controla su propia entra en conflicto.</span><span class="sxs-lookup"><span data-stu-id="ca444-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="ca444-127">**IsInConflict** devuelve S_FALSE si el formulario controla su propia entra en conflicto.</span><span class="sxs-lookup"><span data-stu-id="ca444-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="ca444-128">Un formulario que no administran sus propio conflictos se debe abrir con el método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) y no puede volver a usar un objeto de formulario existente.</span><span class="sxs-lookup"><span data-stu-id="ca444-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ca444-129">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ca444-129">Notes to callers</span></span>

<span data-ttu-id="ca444-130">Las aplicaciones cliente suelen tengan que abordar los problemas con conflictos al mover las aplicaciones de un mensaje para el mensaje siguiente o anterior en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ca444-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="ca444-131">Si un mensaje está en conflicto, pero el servidor de formulario para ese mensaje puede controlar conflictos, la aplicación cliente debe ejecutar su código habitual para mostrar el mensaje siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="ca444-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="ca444-132">Si el servidor de formulario no puede controlar conflictos, la aplicación cliente debe seguir como si era consciente de la clase de mensaje del mensaje siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="ca444-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca444-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="ca444-133">See also</span></span>



[<span data-ttu-id="ca444-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="ca444-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="ca444-135">Propiedad canónico PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="ca444-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="ca444-136">Propiedad canónico PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ca444-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="ca444-137">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca444-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

