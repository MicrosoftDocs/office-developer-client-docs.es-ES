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
# <a name="imapisupportcopymessages"></a><span data-ttu-id="e7fd1-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="e7fd1-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="e7fd1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7fd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7fd1-105">Copia o mueve mensajes de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e7fd1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e7fd1-106">Parameters</span></span>

 <span data-ttu-id="e7fd1-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="e7fd1-108">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta que contiene los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="e7fd1-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="e7fd1-110">a Un puntero a la carpeta que contiene los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="e7fd1-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="e7fd1-112">a Puntero a una matriz de identificadores de entrada que identifican los mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="e7fd1-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="e7fd1-114">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la carpeta de destino para los mensajes copiados o movidos.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="e7fd1-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="e7fd1-116">a Un puntero a la carpeta de destino para los mensajes copiados o movidos.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="e7fd1-117">Esta carpeta debe estar abierta.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-117">This folder must be open.</span></span>
    
 <span data-ttu-id="e7fd1-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="e7fd1-119">a Un puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="e7fd1-120">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="e7fd1-121">El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="e7fd1-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-122">_lpProgress_</span></span>
  
> <span data-ttu-id="e7fd1-123">a Un puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="e7fd1-124">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="e7fd1-125">El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="e7fd1-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7fd1-126">_ulFlags_</span></span>
  
> <span data-ttu-id="e7fd1-127">a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="e7fd1-128">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="e7fd1-128">The following flags can be set:</span></span>
    
<span data-ttu-id="e7fd1-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e7fd1-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="e7fd1-130">Solicita la presentación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="e7fd1-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="e7fd1-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="e7fd1-132">Los mensajes se deben mover, en lugar de copiarse.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="e7fd1-133">Si no se establece MESSAGE_MOVE, se copian los mensajes.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7fd1-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7fd1-134">Return value</span></span>

<span data-ttu-id="e7fd1-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7fd1-135">S_OK</span></span> 
  
> <span data-ttu-id="e7fd1-136">La operación de copia o movimiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="e7fd1-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e7fd1-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e7fd1-138">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e7fd1-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7fd1-139">Remarks</span></span>

<span data-ttu-id="e7fd1-140">El método **IMAPISupport:: CopyMessages** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="e7fd1-141">Los proveedores de almacenamiento de mensajes pueden llamar a **IMAPISupport:: CopyMessages** en su implementación de [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) para copiar o mover uno o más mensajes de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="e7fd1-142">Como parte de la llamada a **IMAPISupport:: CopyMessages** , el proveedor de almacenamiento de mensajes puede especificar que MAPI debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7fd1-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="e7fd1-143">See also</span></span>



[<span data-ttu-id="e7fd1-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="e7fd1-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="e7fd1-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7fd1-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

