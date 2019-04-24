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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341723"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="b7a0c-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="b7a0c-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="b7a0c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7a0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7a0c-105">Muestra un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones en particular.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b7a0c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b7a0c-106">Parameters</span></span>

 <span data-ttu-id="b7a0c-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="b7a0c-108">a Un puntero a un controlador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="b7a0c-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="b7a0c-110">a Un puntero a una función basada en el prototipo [DISMISSMODELESS](dismissmodeless.md) o null.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="b7a0c-111">Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="b7a0c-112">MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo Dirección no modal, para informar a un cliente que está llamando **detalles** que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="b7a0c-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="b7a0c-114">a Un puntero a la información de contexto que se va a pasar a la función **DISMISSMODELESS** señalada por el parámetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="b7a0c-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="b7a0c-115">Este parámetro solo se aplica a la versión no modal del cuadro de diálogo, al incluir la marca DIALOG_SDI en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b7a0c-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b7a0c-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="b7a0c-117">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b7a0c-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b7a0c-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="b7a0c-119">a Un puntero al identificador de entrada de la entrada para la que se muestran los detalles.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="b7a0c-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="b7a0c-121">a Un puntero a una función basada en el prototipo de función [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a0c-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="b7a0c-122">Una función **LPFNBUTTON** agrega un botón al cuadro de diálogo Detalles.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="b7a0c-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="b7a0c-124">a Puntero a los datos que se usaron como parámetro para la función especificada por el parámetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="b7a0c-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="b7a0c-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="b7a0c-126">a Un puntero a una cadena que contiene el texto que se va a aplicar al botón agregado, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="b7a0c-127">El parámetro _lpszButtonText_ debe ser null si no necesita un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="b7a0c-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b7a0c-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b7a0c-129">a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="b7a0c-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="b7a0c-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b7a0c-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="b7a0c-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b7a0c-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="b7a0c-132">Indica que **detalles** Devuelve S_OK si los cambios se realizan realmente en la dirección; de lo contrario, **detalles** devuelve S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="b7a0c-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b7a0c-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="b7a0c-134">Mostrar la versión modal del cuadro de diálogo Dirección común, que siempre se muestra en clientes que no son de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="b7a0c-135">Esta marca se excluye mutuamente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="b7a0c-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="b7a0c-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="b7a0c-137">Mostrar la versión no modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="b7a0c-138">Esta marca se omite para clientes que no son de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="b7a0c-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b7a0c-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b7a0c-140">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b7a0c-141">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7a0c-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7a0c-142">Return value</span></span>

<span data-ttu-id="b7a0c-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7a0c-143">S_OK</span></span> 
  
> <span data-ttu-id="b7a0c-144">El cuadro de diálogo Detalles se mostró correctamente para la entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7a0c-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7a0c-145">Remarks</span></span>

<span data-ttu-id="b7a0c-146">Las aplicaciones cliente llaman \*\*\*\* al método details para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="b7a0c-147">Puede usar los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ para agregar un botón definido por el cliente al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="b7a0c-148">Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada a la que apunta _lpfButtonCallback_y pasa el identificador de entrada del botón y los datos de _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="b7a0c-149">Si no necesita un botón extensible, _lpszButtonText_ debe ser null.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="b7a0c-150">Los **detalles** son compatibles con las cadenas de caracteres Unicode; Las cadenas Unicode se convierten en el formato de cadena de caracteres multibyte (MBCS) antes de que se muestren en el cuadro de diálogo Detalles.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b7a0c-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b7a0c-151">MFCMAPI reference</span></span>

<span data-ttu-id="b7a0c-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b7a0c-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b7a0c-153">**File**</span></span>|<span data-ttu-id="b7a0c-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="b7a0c-154">**Function**</span></span>|<span data-ttu-id="b7a0c-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b7a0c-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7a0c-156">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="b7a0c-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="b7a0c-157">CBaseDialog:: OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="b7a0c-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="b7a0c-158">MFCMAPI usa el \*\*\*\* método details para mostrar un cuadro de diálogo que muestra los detalles de una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b7a0c-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7a0c-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7a0c-159">See also</span></span>



[<span data-ttu-id="b7a0c-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="b7a0c-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="b7a0c-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="b7a0c-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="b7a0c-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="b7a0c-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="b7a0c-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b7a0c-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="b7a0c-164">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b7a0c-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

