---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10f8f2cf44bf1a8e00f8c2b1a76826db5fc07161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817118"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="2b390-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="2b390-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="2b390-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b390-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b390-105">Muestra el cuadro de diálogo de la libreta de direcciones de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2b390-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="2b390-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b390-106">Parameters</span></span>

 <span data-ttu-id="2b390-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2b390-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="2b390-108">[entrada, salida] Un puntero a un identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2b390-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="2b390-109">En la entrada, siempre se debe pasar un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="2b390-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="2b390-110">En la salida, si el miembro **ulFlags** del parámetro _lpAdrParms_ se establece en DIALOG_SDI, se devuelve el identificador de ventana del cuadro de diálogo no modal.</span><span class="sxs-lookup"><span data-stu-id="2b390-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="2b390-111">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2b390-111">See Remarks.</span></span> 
    
 <span data-ttu-id="2b390-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="2b390-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="2b390-113">[entrada, salida] Un puntero a una estructura [ADRPARM](adrparm.md) que controla la presentación y el comportamiento del cuadro de diálogo dirección.</span><span class="sxs-lookup"><span data-stu-id="2b390-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="2b390-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="2b390-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="2b390-115">[entrada, salida] Un puntero a un puntero a una estructura [ADRLIST](adrlist.md) que contiene la información del destinatario.</span><span class="sxs-lookup"><span data-stu-id="2b390-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="2b390-116">En la entrada, este parámetro puede ser NULL o elija un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="2b390-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="2b390-117">En la salida, este parámetro señala a un puntero a la información de destinatario válido.</span><span class="sxs-lookup"><span data-stu-id="2b390-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2b390-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b390-118">Return value</span></span>

<span data-ttu-id="2b390-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b390-119">S_OK</span></span> 
  
> <span data-ttu-id="2b390-120">El cuadro de diálogo común de dirección se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b390-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b390-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b390-121">Remarks</span></span>

<span data-ttu-id="2b390-122">Si el miembro **ulFlags** del parámetro _lpAdrParms_ se establece en DIALOG_SDI prever el retorno del identificador de ventana del cuadro de diálogo no modal de salida, se omite en Outlook; la versión del cuadro de diálogo modal siempre se muestra en los clientes de Outlook que no sean.</span><span class="sxs-lookup"><span data-stu-id="2b390-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="2b390-123">La estructura **ADRLIST** pasada back MAPI al autor de la llamada a través del parámetro _lppAdrList_ contiene una matriz de estructuras [ADRENTRY](adrentry.md) , una estructura para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="2b390-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="2b390-124">Cuando se pasa al método de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de un mensaje saliente en el parámetro _lpMods_ , la estructura **ADRLIST** puede utilizarse para actualizar su lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="2b390-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="2b390-125">Cada estructura **ADRENTRY** en la estructura **ADRLIST** contiene cero o más estructuras de [SPropValue](spropvalue.md) , una estructura para cada conjunto de propiedades para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="2b390-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="2b390-126">Puede haber cero estructuras **SPropValue** cuando el cuadro de diálogo presentado por el método de **dirección** se usa para quitar a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="2b390-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="2b390-127">Cuando hay una o más estructuras de **SPropValue** , la estructura **ADRENTRY** correspondiente se utiliza para agregar o actualizar a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="2b390-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="2b390-128">El destinatario puede ser resuelto, lo que indica que una de las estructuras de **SPropValue** describe la propiedad del destinatario **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o sin resolver, lo que indica que la propiedad de **entrada del objeto** es falta.</span><span class="sxs-lookup"><span data-stu-id="2b390-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="2b390-129">Además de **entrada del objeto**resueltos destinatarios incluyen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="2b390-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="2b390-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b390-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b390-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b390-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b390-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b390-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="2b390-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2b390-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="2b390-134">Es posible que la estructura **ADRLIST** que el autor de la llamada que se pasa en un tamaño diferente de la estructura que se devuelve de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2b390-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="2b390-135">Si MAPI debe devolver una estructura **ADRLIST** más grande, libera la estructura original y asigna una nueva.</span><span class="sxs-lookup"><span data-stu-id="2b390-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="2b390-136">Al asignar memoria para la estructura **ADRLIST** , asignar la memoria para cada estructura **SPropValue** por separado.</span><span class="sxs-lookup"><span data-stu-id="2b390-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="2b390-137">Para obtener más información acerca de cómo asignar y liberar estructuras **ADRLIST** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="2b390-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="2b390-138">**Dirección** se devuelve inmediatamente si la marca DIALOG_SDI se establece en el miembro **ulFlags** de la estructura **ADRPARM** en el parámetro _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="2b390-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="2b390-139">El indicador DIALOG_SDI se omite para los clientes de Outlook que no sean.</span><span class="sxs-lookup"><span data-stu-id="2b390-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="2b390-140">Si se omite la DIALOG_SDI, se mostrará la versión del cuadro de diálogo modal y no se debe esperar un puntero a un identificador en _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="2b390-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="2b390-141">**Dirección** admite cadenas de caracteres Unicode en la estructura **ADRPARM** si AB_UNICODEUI se especificó en el miembro **ulFlags** de **ADRPARM** en el parámetro _lpAdrParms_ , y admite las cadenas de caracteres Unicode en ** ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="2b390-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="2b390-142">Las cadenas de Unicode se convierten en el formato de caracteres de varios bytes (MBCS) de la cadena antes de que se muestren en el cuadro de diálogo de la libreta de direcciones de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2b390-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2b390-143">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2b390-143">MFCMAPI reference</span></span>

<span data-ttu-id="2b390-144">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2b390-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2b390-145">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2b390-145">**File**</span></span>|<span data-ttu-id="2b390-146">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="2b390-146">**Function**</span></span>|<span data-ttu-id="2b390-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2b390-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b390-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2b390-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2b390-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="2b390-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="2b390-150">MFCMAPI utiliza el método de **dirección** para permitir al usuario seleccionar qué buzón para abrir.</span><span class="sxs-lookup"><span data-stu-id="2b390-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b390-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b390-151">See also</span></span>



[<span data-ttu-id="2b390-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="2b390-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="2b390-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2b390-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="2b390-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="2b390-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="2b390-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="2b390-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="2b390-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="2b390-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="2b390-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="2b390-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="2b390-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="2b390-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="2b390-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2b390-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2b390-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="2b390-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="2b390-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2b390-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2b390-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2b390-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="2b390-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="2b390-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="2b390-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2b390-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="2b390-165">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2b390-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="2b390-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2b390-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

