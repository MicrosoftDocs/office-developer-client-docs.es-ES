---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 93f264cc91118e40f7a2869d29e7e53d404ae381
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817651"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="dd4fb-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="dd4fb-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="dd4fb-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd4fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd4fb-105">Elimina un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dd4fb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd4fb-106">Parameters</span></span>

 <span data-ttu-id="dd4fb-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="dd4fb-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="dd4fb-108">[entrada] Número de índice de los datos adjuntos para eliminar.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="dd4fb-109">Éste es el valor de propiedad de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="dd4fb-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dd4fb-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="dd4fb-111">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="dd4fb-112">El parámetro _ulUIParam_ se omite a menos que se establece la marca ATTACH_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="dd4fb-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dd4fb-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="dd4fb-113">_lpProgress_</span></span>
  
> <span data-ttu-id="dd4fb-114">[entrada] Puntero a un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="dd4fb-115">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensaje muestra un indicador de progreso mediante la implementación de objeto de progreso MAPI.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="dd4fb-116">El parámetro _lpProgress_ se omite a menos que se establece la marca ATTACH_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="dd4fb-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd4fb-117">_ulFlags_</span></span>
  
> <span data-ttu-id="dd4fb-118">[entrada] Máscara de bits de indicadores que controla la presentación de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="dd4fb-119">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd4fb-119">The following flag can be set:</span></span>
    
<span data-ttu-id="dd4fb-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="dd4fb-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="dd4fb-121">Solicita la visualización de un indicador de progreso mientras se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd4fb-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd4fb-122">Return value</span></span>

<span data-ttu-id="dd4fb-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd4fb-123">S_OK</span></span> 
  
> <span data-ttu-id="dd4fb-124">Los datos adjuntos se eliminan correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd4fb-125">Notas</span><span class="sxs-lookup"><span data-stu-id="dd4fb-125">Remarks</span></span>

<span data-ttu-id="dd4fb-126">El método **IMessage::DeleteAttach** elimina los datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="dd4fb-127">Un dato adjunto eliminado no se elimina de manera permanente hasta que se ha llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dd4fb-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dd4fb-128">Notes to callers</span></span>

<span data-ttu-id="dd4fb-129">Antes de llamar a **DeleteAttach**, llame al método **IUnknown:: Release** para los datos adjuntos y cada uno de sus secuencias.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="dd4fb-130">Debido a que la eliminación de un archivo adjunto puede ser un proceso largo, **DeleteAttach** proporciona el mecanismo que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="dd4fb-131">Puede solicitar la visualización de un indicador de progreso pasando un puntero a su [IMAPIProgress: IUnknown](imapiprogressiunknown.md) implementación o NULL si no tiene una implementación.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="dd4fb-132">También debe especificar un identificador de ventana en el parámetro _ulUIParam_ y el indicador ATTACH_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="dd4fb-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dd4fb-133">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dd4fb-133">MFCMAPI reference</span></span>

<span data-ttu-id="dd4fb-134">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dd4fb-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="dd4fb-135">**File**</span></span>|<span data-ttu-id="dd4fb-136">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="dd4fb-136">**Function**</span></span>|<span data-ttu-id="dd4fb-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="dd4fb-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd4fb-138">AttachmentsDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dd4fb-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="dd4fb-139">CAttachmentsDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="dd4fb-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="dd4fb-140">MFCMAPI usa el método **IMessage::DeleteAttach** para eliminar los datos adjuntos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd4fb-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="dd4fb-141">See also</span></span>



[<span data-ttu-id="dd4fb-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dd4fb-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="dd4fb-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dd4fb-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="dd4fb-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="dd4fb-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

