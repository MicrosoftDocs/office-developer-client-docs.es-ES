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
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591040"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="fdb76-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="fdb76-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="fdb76-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdb76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdb76-105">Copia o mueve los mensajes de una carpeta a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="fdb76-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="fdb76-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdb76-106">Parameters</span></span>

 <span data-ttu-id="fdb76-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="fdb76-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="fdb76-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta que contiene los mensajes que se pueden copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="fdb76-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="fdb76-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="fdb76-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="fdb76-110">[entrada] Un puntero a la carpeta que contiene los mensajes que se pueden copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="fdb76-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="fdb76-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="fdb76-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="fdb76-112">[entrada] Un puntero a una matriz de identificadores de entrada que identifican los mensajes para ser copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="fdb76-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="fdb76-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="fdb76-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="fdb76-114">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la carpeta de destino para los mensajes que se ha movido o copiados.</span><span class="sxs-lookup"><span data-stu-id="fdb76-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="fdb76-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="fdb76-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="fdb76-116">[entrada] Un puntero a la carpeta de destino para los mensajes que se ha movido o copiados.</span><span class="sxs-lookup"><span data-stu-id="fdb76-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="fdb76-117">Esta carpeta debe estar abierta.</span><span class="sxs-lookup"><span data-stu-id="fdb76-117">This folder must be open.</span></span>
    
 <span data-ttu-id="fdb76-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fdb76-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="fdb76-119">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="fdb76-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="fdb76-120">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdb76-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="fdb76-121">El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="fdb76-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="fdb76-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="fdb76-122">_lpProgress_</span></span>
  
> <span data-ttu-id="fdb76-123">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="fdb76-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="fdb76-124">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante el uso de la implementación del objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdb76-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="fdb76-125">El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="fdb76-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="fdb76-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fdb76-126">_ulFlags_</span></span>
  
> <span data-ttu-id="fdb76-127">[entrada] Una máscara de bits de indicadores que controla cómo se lleva a cabo la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="fdb76-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="fdb76-128">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="fdb76-128">The following flags can be set:</span></span>
    
<span data-ttu-id="fdb76-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="fdb76-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="fdb76-130">Solicita la visualización de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="fdb76-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="fdb76-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="fdb76-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="fdb76-132">Se va a mover los mensajes, en lugar de copiado.</span><span class="sxs-lookup"><span data-stu-id="fdb76-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="fdb76-133">Si no se establece MESSAGE_MOVE, se copian los mensajes.</span><span class="sxs-lookup"><span data-stu-id="fdb76-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fdb76-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdb76-134">Return value</span></span>

<span data-ttu-id="fdb76-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="fdb76-135">S_OK</span></span> 
  
> <span data-ttu-id="fdb76-136">La operación de copiar o mover fue correcta.</span><span class="sxs-lookup"><span data-stu-id="fdb76-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="fdb76-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="fdb76-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="fdb76-138">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fdb76-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fdb76-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdb76-139">Remarks</span></span>

<span data-ttu-id="fdb76-140">El método **IMAPISupport::CopyMessages** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fdb76-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="fdb76-141">Los proveedores de almacén de mensajes pueden llamar a **IMAPISupport::CopyMessages** en su implementación de [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar o mover uno o más mensajes de una carpeta a otra.</span><span class="sxs-lookup"><span data-stu-id="fdb76-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="fdb76-142">Como parte de la llamada **IMAPISupport::CopyMessages** , puede especificar el proveedor de almacén de mensajes que MAPI debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="fdb76-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fdb76-143">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fdb76-143">See also</span></span>



[<span data-ttu-id="fdb76-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="fdb76-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="fdb76-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fdb76-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

