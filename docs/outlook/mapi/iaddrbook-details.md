---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424682"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="24b93-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="24b93-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="24b93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24b93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24b93-105">Muestra un cuadro de diálogo que muestra detalles sobre una entrada de libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="24b93-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="24b93-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="24b93-106">Parameters</span></span>

 <span data-ttu-id="24b93-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="24b93-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="24b93-108">[in] Puntero a un controlador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="24b93-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="24b93-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="24b93-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="24b93-110">[in] Puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL.</span><span class="sxs-lookup"><span data-stu-id="24b93-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="24b93-111">Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="24b93-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="24b93-112">MAPI llama a **la función DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a **Details** de que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="24b93-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="24b93-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="24b93-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="24b93-114">[in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="24b93-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="24b93-115">Este parámetro solo se aplica a la versión modeless del cuadro de diálogo, incluyendo la marca DIALOG_SDI en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="24b93-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="24b93-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="24b93-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="24b93-117">[in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="24b93-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="24b93-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="24b93-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="24b93-119">[in] Puntero al identificador de entrada de la entrada para la que se muestran los detalles.</span><span class="sxs-lookup"><span data-stu-id="24b93-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="24b93-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="24b93-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="24b93-121">[in] Puntero a una función basada en el prototipo de función [LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="24b93-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="24b93-122">Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="24b93-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="24b93-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="24b93-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="24b93-124">[in] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="24b93-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="24b93-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="24b93-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="24b93-126">[in] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="24b93-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="24b93-127">El  _parámetro lpszButtonText_ debe ser NULL si no necesita un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="24b93-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="24b93-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24b93-128">_ulFlags_</span></span>
  
> <span data-ttu-id="24b93-129">[in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="24b93-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="24b93-130">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="24b93-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="24b93-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="24b93-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="24b93-132">Indica que **Details** devuelve S_OK si realmente se realizan cambios en la dirección; de lo contrario, **Details** devuelve S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="24b93-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="24b93-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="24b93-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="24b93-134">Muestra la versión modal del cuadro de diálogo dirección común, que siempre se muestra en clientes que no Outlook direcciones.</span><span class="sxs-lookup"><span data-stu-id="24b93-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="24b93-135">Esta marca es mutuamente exclusiva con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="24b93-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="24b93-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="24b93-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="24b93-137">Mostrar la versión modeless del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="24b93-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="24b93-138">Esta marca se omite para clientes que no Outlook cliente.</span><span class="sxs-lookup"><span data-stu-id="24b93-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="24b93-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="24b93-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="24b93-140">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="24b93-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="24b93-141">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="24b93-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24b93-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24b93-142">Return value</span></span>

<span data-ttu-id="24b93-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="24b93-143">S_OK</span></span> 
  
> <span data-ttu-id="24b93-144">El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="24b93-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24b93-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24b93-145">Remarks</span></span>

<span data-ttu-id="24b93-146">Las aplicaciones cliente llaman al **método Details** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="24b93-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="24b93-147">Puede usar los parámetros  _lpfButtonCallback_,  _lpvButtonContext_ y  _lpszButtonText_ para agregar un botón definido por el cliente al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="24b93-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="24b93-148">Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada señalada por  _lpfButtonCallback_, pasando tanto el identificador de entrada del botón como los datos de  _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="24b93-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="24b93-149">Si no necesita un botón extensible,  _lpszButtonText_ debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="24b93-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="24b93-150">**Los detalles** admiten cadenas de caracteres Unicode; Las cadenas Unicode se convierten al formato de cadena de caracteres multibyte (MBCS) antes de que se muestren en el cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="24b93-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24b93-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24b93-151">MFCMAPI reference</span></span>

<span data-ttu-id="24b93-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="24b93-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24b93-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="24b93-153">**File**</span></span>|<span data-ttu-id="24b93-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="24b93-154">**Function**</span></span>|<span data-ttu-id="24b93-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="24b93-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24b93-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="24b93-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="24b93-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="24b93-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="24b93-158">MFCMAPI usa el **método Details** para mostrar un cuadro de diálogo que muestra los detalles de una entrada de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="24b93-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24b93-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="24b93-159">See also</span></span>



[<span data-ttu-id="24b93-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="24b93-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="24b93-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="24b93-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="24b93-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="24b93-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="24b93-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="24b93-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="24b93-164">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="24b93-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

