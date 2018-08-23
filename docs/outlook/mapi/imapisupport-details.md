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
ms.openlocfilehash: 3c1bfccf635b96dd0744d888e69b4af5b8df0fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587876"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="54396-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="54396-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="54396-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54396-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54396-105">Muestra un cuadro de diálogo que muestra detalles acerca de una entrada de la libreta de direcciones determinada.</span><span class="sxs-lookup"><span data-stu-id="54396-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="54396-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54396-106">Parameters</span></span>

 <span data-ttu-id="54396-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="54396-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="54396-108">[out] Un puntero al identificador de la ventana principal del cuadro de diálogo devuelto.</span><span class="sxs-lookup"><span data-stu-id="54396-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="54396-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="54396-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="54396-110">[entrada] Un puntero a una función basándose en el prototipo [DISMISSMODELESS](dismissmodeless.md) o NULL.</span><span class="sxs-lookup"><span data-stu-id="54396-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="54396-111">Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="54396-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="54396-112">MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a **IMAPISupport::Details** que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="54396-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="54396-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="54396-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="54396-114">[entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="54396-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="54396-115">Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca DIALOG_SDI en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="54396-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="54396-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="54396-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="54396-117">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="54396-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="54396-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="54396-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="54396-119">[entrada] Un puntero al identificador de entrada para la que se muestran los detalles.</span><span class="sxs-lookup"><span data-stu-id="54396-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="54396-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="54396-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="54396-121">[entrada] Un puntero a una función según el prototipo de función [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="54396-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="54396-122">Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="54396-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="54396-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="54396-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="54396-124">[entrada] Un puntero a datos que se usa como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="54396-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="54396-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="54396-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="54396-126">[entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="54396-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="54396-127">El parámetro _lpszButtonText_ debe ser NULL si no se necesita un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="54396-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="54396-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54396-128">_ulFlags_</span></span>
  
> <span data-ttu-id="54396-129">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="54396-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="54396-130">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="54396-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="54396-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="54396-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="54396-132">Mostrar la versión modal del cuadro de diálogo dirección comunes.</span><span class="sxs-lookup"><span data-stu-id="54396-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="54396-133">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="54396-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="54396-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="54396-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="54396-135">Mostrar la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="54396-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="54396-136">Este marcador es mutuamente excluyente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="54396-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="54396-137">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="54396-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="54396-138">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="54396-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="54396-139">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="54396-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54396-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54396-140">Return value</span></span>

<span data-ttu-id="54396-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="54396-141">S_OK</span></span> 
  
> <span data-ttu-id="54396-142">El cuadro de diálogo detalles se mostró correctamente para la entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="54396-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54396-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54396-143">Remarks</span></span>

<span data-ttu-id="54396-144">El método **IMAPISupport::Details** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="54396-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="54396-145">Los proveedores de la libreta de direcciones, llame a **Detalles** para mostrar un cuadro de diálogo que proporciona detalles sobre una entrada determinada en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="54396-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="54396-146">Los parámetros _lpfButtonCallback_, _lpvButtonContext_y _lpszButtonText_ se pueden usar para agregar un botón definido por el cliente para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="54396-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="54396-147">Cuando se hace clic en el botón, MAPI llama a la función de devolución de llamada que apunta _lpfButtonCallback_, pasando el identificador de entrada de los datos y el botón en _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="54396-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="54396-148">Si no es necesario un botón extensible, _lpszButtonText_ debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="54396-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54396-149">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="54396-149">See also</span></span>



[<span data-ttu-id="54396-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="54396-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="54396-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="54396-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="54396-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="54396-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="54396-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="54396-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

