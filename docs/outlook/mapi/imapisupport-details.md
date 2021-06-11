---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426782"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="3d82d-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="3d82d-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="3d82d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d82d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d82d-105">Muestra un cuadro de diálogo que muestra detalles sobre una entrada de libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="3d82d-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3d82d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3d82d-106">Parameters</span></span>

 <span data-ttu-id="3d82d-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3d82d-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="3d82d-108">[salida] Puntero al controlador a la ventana primaria del cuadro de diálogo devuelto.</span><span class="sxs-lookup"><span data-stu-id="3d82d-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="3d82d-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="3d82d-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="3d82d-110">[in] Puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL.</span><span class="sxs-lookup"><span data-stu-id="3d82d-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="3d82d-111">Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="3d82d-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="3d82d-112">MAPI llama a la función **DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a **IMAPISupport::D etails** que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="3d82d-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="3d82d-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="3d82d-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="3d82d-114">[in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="3d82d-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="3d82d-115">Este parámetro solo se aplica a la versión modeless del cuadro de diálogo, incluyendo la marca DIALOG_SDI en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="3d82d-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="3d82d-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3d82d-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="3d82d-117">[in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="3d82d-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3d82d-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3d82d-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="3d82d-119">[in] Puntero al identificador de entrada para el que se muestran los detalles.</span><span class="sxs-lookup"><span data-stu-id="3d82d-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="3d82d-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="3d82d-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="3d82d-121">[in] Puntero a una función basada en el prototipo de función [LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="3d82d-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="3d82d-122">Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="3d82d-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="3d82d-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="3d82d-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="3d82d-124">[in] Puntero a los datos usados como parámetro para la función especificada por el _parámetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="3d82d-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="3d82d-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="3d82d-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="3d82d-126">[in] Puntero a una cadena que contiene texto que se aplicará al botón agregado si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="3d82d-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="3d82d-127">El  _parámetro lpszButtonText_ debe ser NULL si no se necesita un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="3d82d-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="3d82d-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d82d-128">_ulFlags_</span></span>
  
> <span data-ttu-id="3d82d-129">[in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="3d82d-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="3d82d-130">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="3d82d-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="3d82d-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="3d82d-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="3d82d-132">Mostrar la versión modal del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="3d82d-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="3d82d-133">Esta marca es mutuamente exclusiva con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="3d82d-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="3d82d-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="3d82d-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="3d82d-135">Mostrar la versión modeless del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="3d82d-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="3d82d-136">Esta marca es mutuamente exclusiva con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="3d82d-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="3d82d-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3d82d-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3d82d-138">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3d82d-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="3d82d-139">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3d82d-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d82d-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d82d-140">Return value</span></span>

<span data-ttu-id="3d82d-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d82d-141">S_OK</span></span> 
  
> <span data-ttu-id="3d82d-142">El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3d82d-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d82d-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d82d-143">Remarks</span></span>

<span data-ttu-id="3d82d-144">El **método IMAPISupport::D etails** se implementa para objetos de soporte del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3d82d-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="3d82d-145">Los proveedores de libreta de direcciones llaman a **Detalles** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="3d82d-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="3d82d-146">Los  _parámetros lpfButtonCallback_,  _lpvButtonContext_ y  _lpszButtonText_ se pueden usar para agregar un botón definido por el cliente al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3d82d-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="3d82d-147">Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada señalada por  _lpfButtonCallback_, pasando tanto el identificador de entrada del botón como los datos de  _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="3d82d-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="3d82d-148">Si no se necesita un botón extensible,  _lpszButtonText_ debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="3d82d-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d82d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d82d-149">See also</span></span>



[<span data-ttu-id="3d82d-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="3d82d-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="3d82d-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="3d82d-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="3d82d-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="3d82d-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="3d82d-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d82d-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

