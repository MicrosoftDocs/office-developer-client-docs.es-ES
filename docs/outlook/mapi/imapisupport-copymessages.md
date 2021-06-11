---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405159"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="1272d-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1272d-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="1272d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1272d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1272d-105">Copia o mueve mensajes de una carpeta a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="1272d-105">Copies or moves messages from one folder to another folder.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1272d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1272d-106">Parameters</span></span>

 <span data-ttu-id="1272d-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="1272d-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="1272d-108">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta que contiene los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1272d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="1272d-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="1272d-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="1272d-110">[in] Puntero a la carpeta que contiene los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1272d-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="1272d-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="1272d-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="1272d-112">[in] Puntero a una matriz de identificadores de entrada que identifican los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1272d-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="1272d-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="1272d-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="1272d-114">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino de los mensajes copiados o movidos.</span><span class="sxs-lookup"><span data-stu-id="1272d-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="1272d-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="1272d-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="1272d-116">[in] Puntero a la carpeta de destino de los mensajes copiados o movidos.</span><span class="sxs-lookup"><span data-stu-id="1272d-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="1272d-117">Esta carpeta debe estar abierta.</span><span class="sxs-lookup"><span data-stu-id="1272d-117">This folder must be open.</span></span>
    
 <span data-ttu-id="1272d-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1272d-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="1272d-119">[in] Puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1272d-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1272d-120">Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="1272d-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1272d-121">El  _parámetro lpProgress_ se omite a menos que la marca MESSAGE_DIALOG esté establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="1272d-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1272d-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1272d-122">_lpProgress_</span></span>
  
> <span data-ttu-id="1272d-123">[in] Puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1272d-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="1272d-124">Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="1272d-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="1272d-125">El  _parámetro lpProgress_ se omite a menos que la marca MESSAGE_DIALOG esté establecida en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="1272d-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="1272d-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1272d-126">_ulFlags_</span></span>
  
> <span data-ttu-id="1272d-127">[in] Máscara de bits de marcas que controla cómo se realiza la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="1272d-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="1272d-128">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="1272d-128">The following flags can be set:</span></span>
    
<span data-ttu-id="1272d-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1272d-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="1272d-130">Solicita la presentación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1272d-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="1272d-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="1272d-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="1272d-132">Los mensajes deben moverse, en lugar de copiarse.</span><span class="sxs-lookup"><span data-stu-id="1272d-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="1272d-133">Si MESSAGE_MOVE no está establecido, los mensajes se copian.</span><span class="sxs-lookup"><span data-stu-id="1272d-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1272d-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1272d-134">Return value</span></span>

<span data-ttu-id="1272d-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="1272d-135">S_OK</span></span> 
  
> <span data-ttu-id="1272d-136">La operación de copiar o mover se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1272d-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="1272d-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1272d-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1272d-138">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1272d-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1272d-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1272d-139">Remarks</span></span>

<span data-ttu-id="1272d-140">El **método IMAPISupport::CopyMessages** se implementa para objetos de soporte del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1272d-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="1272d-141">Los proveedores de almacén de mensajes pueden llamar a **IMAPISupport::CopyMessages** en su implementación de [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar o mover uno o varios mensajes de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="1272d-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="1272d-142">Como parte de la **llamada IMAPISupport::CopyMessages,** el proveedor del almacén de mensajes puede especificar que MAPI debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1272d-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1272d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1272d-143">See also</span></span>



[<span data-ttu-id="1272d-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1272d-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="1272d-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1272d-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

