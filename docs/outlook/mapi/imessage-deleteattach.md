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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430710"
---
# <a name="imessagedeleteattach"></a><span data-ttu-id="85170-103">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="85170-103">IMessage::DeleteAttach</span></span>

  
  
<span data-ttu-id="85170-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85170-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85170-105">Elimina datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="85170-105">Deletes an attachment.</span></span>
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="85170-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="85170-106">Parameters</span></span>

 <span data-ttu-id="85170-107">_ulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="85170-107">_ulAttachmentNum_</span></span>
  
> <span data-ttu-id="85170-108">a Número de índice de los datos adjuntos que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="85170-108">[in] Index number of the attachment to delete.</span></span> <span data-ttu-id="85170-109">Este es el valor de la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="85170-109">This is the value for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="85170-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="85170-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="85170-111">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que este método muestra.</span><span class="sxs-lookup"><span data-stu-id="85170-111">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="85170-112">El parámetro _ulUIParam_ se omite a menos que se establezca la marca ATTACH_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="85170-112">The  _ulUIParam_ parameter is ignored unless the ATTACH_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="85170-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="85170-113">_lpProgress_</span></span>
  
> <span data-ttu-id="85170-114">a Puntero a un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="85170-114">[in] Pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="85170-115">Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación del objeto de progreso de MAPI.</span><span class="sxs-lookup"><span data-stu-id="85170-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator using the MAPI progress object implementation.</span></span> <span data-ttu-id="85170-116">El parámetro _lpProgress_ se omite a menos que se establezca la marca ATTACH_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="85170-116">The  _lpProgress_ parameter is ignored unless the ATTACH_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="85170-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85170-117">_ulFlags_</span></span>
  
> <span data-ttu-id="85170-118">a Máscara de máscara de marcadores que controla la presentación de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="85170-118">[in] Bitmask of flags that controls the display of a user interface.</span></span> <span data-ttu-id="85170-119">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="85170-119">The following flag can be set:</span></span>
    
<span data-ttu-id="85170-120">ATTACH_DIALOG</span><span class="sxs-lookup"><span data-stu-id="85170-120">ATTACH_DIALOG</span></span> 
  
> <span data-ttu-id="85170-121">Solicita la visualización de un indicador de progreso mientras se lleva a cabo la operación.</span><span class="sxs-lookup"><span data-stu-id="85170-121">Requests the display of a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85170-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85170-122">Return value</span></span>

<span data-ttu-id="85170-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="85170-123">S_OK</span></span> 
  
> <span data-ttu-id="85170-124">Los datos adjuntos se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="85170-124">The attachment was successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85170-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85170-125">Remarks</span></span>

<span data-ttu-id="85170-126">El método **IMessage::D eleteattach** elimina datos adjuntos desde dentro de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="85170-126">The **IMessage::DeleteAttach** method deletes an attachment from within a message.</span></span> 
  
<span data-ttu-id="85170-127">Los datos adjuntos eliminados no se eliminan permanentemente hasta que se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="85170-127">A deleted attachment is not permanently deleted until the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="85170-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="85170-128">Notes to callers</span></span>

<span data-ttu-id="85170-129">Antes de llamar a **DeleteAttach**, llame al método **IUnknown:: Release** para los datos adjuntos y cada una de sus secuencias.</span><span class="sxs-lookup"><span data-stu-id="85170-129">Before calling **DeleteAttach**, call the **IUnknown::Release** method for the attachment and each of its streams.</span></span> 
  
<span data-ttu-id="85170-130">Como la eliminación de datos adjuntos puede ser un proceso prolongado, **DeleteAttach** proporciona el mecanismo que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="85170-130">Because deleting an attachment can be a lengthy process, **DeleteAttach** provides the mechanism that displays a progress indicator.</span></span> <span data-ttu-id="85170-131">Puede solicitar la presentación de un indicador de progreso pasando un puntero a su [método imapiprogress:](imapiprogressiunknown.md) implementación de IUNKNOWN o null si no tiene una implementación.</span><span class="sxs-lookup"><span data-stu-id="85170-131">You can request the display of a progress indicator by passing a pointer to your [IMAPIProgress : IUnknown](imapiprogressiunknown.md) implementation or NULL if you do not have an implementation.</span></span> <span data-ttu-id="85170-132">También debe especificar un identificador de ventana en el parámetro _ulUIParam_ y la marca ATTACH_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="85170-132">You must also specify a window handle in the  _ulUIParam_ parameter and the ATTACH_DIALOG flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="85170-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="85170-133">MFCMAPI reference</span></span>

<span data-ttu-id="85170-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="85170-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="85170-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="85170-135">**File**</span></span>|<span data-ttu-id="85170-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="85170-136">**Function**</span></span>|<span data-ttu-id="85170-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="85170-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="85170-138">AttachmentsDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="85170-138">AttachmentsDlg.cpp</span></span>  <br/> |<span data-ttu-id="85170-139">CAttachmentsDlg:: OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="85170-139">CAttachmentsDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="85170-140">MFCMAPI usa el método **IMessage::D eleteattach** para eliminar los datos adjuntos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="85170-140">MFCMAPI uses the **IMessage::DeleteAttach** method to delete the selected attachment.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85170-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="85170-141">See also</span></span>



[<span data-ttu-id="85170-142">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="85170-142">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="85170-143">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="85170-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="85170-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="85170-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

