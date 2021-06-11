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
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407910"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="90e35-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="90e35-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="90e35-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90e35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90e35-105">Muestra el Outlook de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="90e35-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="90e35-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="90e35-106">Parameters</span></span>

 <span data-ttu-id="90e35-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="90e35-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="90e35-108">[in, out] Puntero a un identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="90e35-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="90e35-109">En la entrada, siempre se debe pasar un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="90e35-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="90e35-110">En el resultado, si el **miembro ulFlags** del parámetro  _lpAdrParms_ se establece en DIALOG_SDI, se devuelve el identificador de ventana del cuadro de diálogo modeless.</span><span class="sxs-lookup"><span data-stu-id="90e35-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="90e35-111">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="90e35-111">See Remarks.</span></span> 
    
 <span data-ttu-id="90e35-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="90e35-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="90e35-113">[in, out] Puntero a una estructura [ADRPARM](adrparm.md) que controla la presentación y el comportamiento del cuadro de diálogo de dirección.</span><span class="sxs-lookup"><span data-stu-id="90e35-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="90e35-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="90e35-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="90e35-115">[in, out] Puntero a un puntero a una [estructura ADRLIST](adrlist.md) que contiene información de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="90e35-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="90e35-116">En la entrada, este parámetro puede ser NULL o apuntar a un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="90e35-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="90e35-117">En el resultado, este parámetro apunta a un puntero a la información de destinatario válida.</span><span class="sxs-lookup"><span data-stu-id="90e35-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="90e35-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90e35-118">Return value</span></span>

<span data-ttu-id="90e35-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="90e35-119">S_OK</span></span> 
  
> <span data-ttu-id="90e35-120">El cuadro de diálogo dirección común se mostró correctamente.</span><span class="sxs-lookup"><span data-stu-id="90e35-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90e35-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90e35-121">Remarks</span></span>

<span data-ttu-id="90e35-122">Si el **miembro ulFlags** del parámetro _lpAdrParms_ se establece en DIALOG_SDI anticipando el retorno del controlador de ventana del cuadro de diálogo modeless en la salida, se omite en Outlook; la versión modal del cuadro de diálogo siempre se muestra en clientes que no Outlook usuario.</span><span class="sxs-lookup"><span data-stu-id="90e35-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="90e35-123">La **estructura ADRLIST** pasada por MAPI al autor de la llamada a través del parámetro  _lppAdrList_ contiene una matriz de estructuras [ADRENTRY,](adrentry.md) una estructura para cada destinatario.</span><span class="sxs-lookup"><span data-stu-id="90e35-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="90e35-124">Cuando se pasa al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) de un mensaje saliente en el parámetro  _lpMods,_ la estructura **ADRLIST** se puede usar para actualizar su lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="90e35-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="90e35-125">Cada **estructura ADRENTRY** de la estructura **ADRLIST** contiene cero o más estructuras [SPropValue,](spropvalue.md) una estructura para cada conjunto de propiedades para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="90e35-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="90e35-126">Puede haber cero **estructuras SPropValue** cuando se usa el cuadro de diálogo presentado por el **método Address** para quitar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="90e35-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="90e35-127">Cuando hay una o varias estructuras **SPropValue,** se usa la estructura **ADRENTRY** correspondiente para agregar o actualizar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="90e35-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="90e35-128">El destinatario puede resolverse, lo que indica que una de las estructuras **SPropValue** describe la propiedad PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) del destinatario, o no resuelto, lo que indica que falta la propiedad **PR_ENTRYID.** </span><span class="sxs-lookup"><span data-stu-id="90e35-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="90e35-129">Además de **PR_ENTRYID**, los destinatarios resueltos incluyen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="90e35-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="90e35-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90e35-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="90e35-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90e35-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="90e35-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90e35-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="90e35-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90e35-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="90e35-134">La **estructura ADRLIST** que pasa el autor de la llamada puede tener un tamaño diferente de la estructura que devuelve MAPI.</span><span class="sxs-lookup"><span data-stu-id="90e35-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="90e35-135">Si MAPI debe devolver una estructura **ADRLIST** más grande, libera la estructura original y asigna una nueva.</span><span class="sxs-lookup"><span data-stu-id="90e35-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="90e35-136">Al asignar memoria para la estructura **ADRLIST,** asigne la memoria para cada **estructura SPropValue por** separado.</span><span class="sxs-lookup"><span data-stu-id="90e35-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="90e35-137">Para obtener más información sobre cómo asignar y liberar estructuras **ADRLIST,** vea [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="90e35-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="90e35-138">**Address** devuelve inmediatamente si la marca DIALOG_SDI se establece en el **miembro ulFlags** de la estructura **ADRPARM** del parámetro _lpAdrParms._</span><span class="sxs-lookup"><span data-stu-id="90e35-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="90e35-139">La DIALOG_SDI se omite para clientes que no Outlook cliente.</span><span class="sxs-lookup"><span data-stu-id="90e35-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="90e35-140">Si DIALOG_SDI se omite, se mostrará la versión modal del cuadro de diálogo y no se debe esperar un puntero a un identificador en  _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="90e35-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="90e35-141">**Address** admite cadenas de caracteres Unicode en la estructura **ADRPARM** si AB_UNICODEUI se especificó en el **miembro ulFlags** de **ADRPARM** en el parámetro  _lpAdrParms_ y admite cadenas de caracteres Unicode en **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="90e35-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="90e35-142">Las cadenas Unicode se convierten al formato de cadena de caracteres multibyte (MBCS) antes de que se muestren en el cuadro de diálogo Outlook libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="90e35-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="90e35-143">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="90e35-143">MFCMAPI reference</span></span>

<span data-ttu-id="90e35-144">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="90e35-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="90e35-145">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="90e35-145">**File**</span></span>|<span data-ttu-id="90e35-146">**Función**</span><span class="sxs-lookup"><span data-stu-id="90e35-146">**Function**</span></span>|<span data-ttu-id="90e35-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="90e35-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90e35-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="90e35-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="90e35-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="90e35-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="90e35-150">MFCMAPI usa el **método Address** para permitir al usuario seleccionar el buzón que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="90e35-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90e35-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="90e35-151">See also</span></span>



[<span data-ttu-id="90e35-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="90e35-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="90e35-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="90e35-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="90e35-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="90e35-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="90e35-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="90e35-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="90e35-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="90e35-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="90e35-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="90e35-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="90e35-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="90e35-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="90e35-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="90e35-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="90e35-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="90e35-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="90e35-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="90e35-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="90e35-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="90e35-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="90e35-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="90e35-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="90e35-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="90e35-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="90e35-165">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="90e35-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="90e35-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="90e35-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

