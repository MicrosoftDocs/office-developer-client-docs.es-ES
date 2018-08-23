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
ms.openlocfilehash: e240ec4e7a61b9e7484f467926501f8c5f5a59f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592349"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="51e83-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="51e83-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="51e83-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51e83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51e83-105">Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="51e83-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="51e83-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51e83-106">Parameters</span></span>

 <span data-ttu-id="51e83-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="51e83-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="51e83-108">[entrada] Un puntero a un identificador de la ventana primaria para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="51e83-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="51e83-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="51e83-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="51e83-110">[entrada] Un puntero a una función basándose en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL.</span><span class="sxs-lookup"><span data-stu-id="51e83-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="51e83-111">Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="51e83-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="51e83-112">MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a **Detalles** que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="51e83-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="51e83-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="51e83-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="51e83-114">[entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="51e83-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="51e83-115">Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca DIALOG_SDI en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="51e83-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="51e83-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="51e83-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="51e83-117">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="51e83-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="51e83-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="51e83-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="51e83-119">[entrada] Un puntero al identificador de entrada de la entrada para la que se muestran los detalles.</span><span class="sxs-lookup"><span data-stu-id="51e83-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="51e83-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="51e83-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="51e83-121">[entrada] Un puntero a una función según el prototipo de función [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="51e83-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="51e83-122">Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="51e83-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="51e83-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="51e83-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="51e83-124">[entrada] Un puntero a los datos que se usan como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="51e83-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="51e83-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="51e83-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="51e83-126">[entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="51e83-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="51e83-127">El parámetro _lpszButtonText_ debe ser NULL si no es necesario un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="51e83-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="51e83-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51e83-128">_ulFlags_</span></span>
  
> <span data-ttu-id="51e83-129">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="51e83-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="51e83-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="51e83-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="51e83-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="51e83-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="51e83-132">Indica que **Detalles** devuelve S_OK si realmente se realizan cambios en la dirección; de lo contrario, **Detalles** devuelve S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="51e83-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="51e83-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="51e83-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="51e83-134">Mostrar la versión del cuadro de diálogo dirección comunes, que siempre se muestra en los clientes de Outlook no modal.</span><span class="sxs-lookup"><span data-stu-id="51e83-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="51e83-135">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="51e83-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="51e83-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="51e83-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="51e83-137">Mostrar la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="51e83-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="51e83-138">Este indicador se omite para los clientes de Outlook que no sean.</span><span class="sxs-lookup"><span data-stu-id="51e83-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="51e83-139">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="51e83-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="51e83-140">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="51e83-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="51e83-141">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="51e83-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51e83-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51e83-142">Return value</span></span>

<span data-ttu-id="51e83-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="51e83-143">S_OK</span></span> 
  
> <span data-ttu-id="51e83-144">El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="51e83-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51e83-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51e83-145">Remarks</span></span>

<span data-ttu-id="51e83-146">Las aplicaciones cliente de llaman al método **Detalles** para mostrar un cuadro de diálogo que proporciona información detallada sobre una entrada determinada en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="51e83-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="51e83-147">Puede usar los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ para agregar un botón definido por el cliente para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="51e83-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="51e83-148">Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada que apunta _lpfButtonCallback_, pasando el identificador de entrada de los datos y el botón en _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="51e83-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="51e83-149">Si no necesita un botón extensible, _lpszButtonText_ debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="51e83-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="51e83-150">**Detalles** admite las cadenas de caracteres Unicode; Las cadenas de Unicode se convierten en el formato de caracteres de varios bytes (MBCS) de la cadena antes de que se muestren en el cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="51e83-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="51e83-151">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="51e83-151">MFCMAPI reference</span></span>

<span data-ttu-id="51e83-152">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="51e83-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="51e83-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="51e83-153">**File**</span></span>|<span data-ttu-id="51e83-154">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="51e83-154">**Function**</span></span>|<span data-ttu-id="51e83-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="51e83-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51e83-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="51e83-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="51e83-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="51e83-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="51e83-158">MFCMAPI usa el método **Details** para mostrar un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="51e83-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51e83-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="51e83-159">See also</span></span>



[<span data-ttu-id="51e83-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="51e83-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="51e83-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="51e83-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="51e83-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="51e83-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="51e83-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51e83-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="51e83-164">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="51e83-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

