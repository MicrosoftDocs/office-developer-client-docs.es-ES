---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb4f38615ac6cacb3acbaa456f0992bf55c3653d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568626"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="b9918-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="b9918-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="b9918-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9918-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9918-105">Se asegura de que se abre el método **OpenEntry** por el proveedor de la libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="b9918-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="b9918-106">Esta función funciona de manera similar a [IAddrBook::Details](iaddrbook-details.md) , pero abre **entryID** utilizando la libreta de direcciones de Exchange identificada por _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="b9918-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9918-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b9918-107">Header file:</span></span>  <br/> |<span data-ttu-id="b9918-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="b9918-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="b9918-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b9918-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="b9918-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="b9918-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="b9918-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b9918-111">Called by:</span></span>  <br/> |<span data-ttu-id="b9918-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b9918-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b9918-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9918-113">Parameters</span></span>

 <span data-ttu-id="b9918-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="b9918-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="b9918-115">[entrada] Un puntero a un _emsabpUID_ que identifica el proveedor de la libreta de direcciones de Exchange debe usar esta función para mostrar detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9918-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="b9918-116">Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de la libreta de direcciones, este parámetro se omite y el actúa de llamada de función exactamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="b9918-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="b9918-117">Si este parámetro es NULL o un cero MAPIUID, esta función también actúa exactamente igual que [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="b9918-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="b9918-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="b9918-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="b9918-119">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9918-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="b9918-120">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b9918-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="b9918-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b9918-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="b9918-122">[out] Identificador de la ventana primaria para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9918-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="b9918-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="b9918-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="b9918-124">[entrada] Un puntero a una función basándose en el prototipo **DISMISSMODELESS** o NULL.</span><span class="sxs-lookup"><span data-stu-id="b9918-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="b9918-125">Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b9918-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="b9918-126">MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a detalles que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="b9918-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="b9918-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="b9918-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="b9918-128">[entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="b9918-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="b9918-129">Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca **DIALOG_SDI** en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="b9918-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b9918-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b9918-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="b9918-131">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b9918-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b9918-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b9918-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="b9918-133">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="b9918-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="b9918-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="b9918-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="b9918-135">[entrada] Un puntero a una función según el prototipo de función **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="b9918-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="b9918-136">Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="b9918-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="b9918-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="b9918-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="b9918-138">[entrada] Un puntero a los datos que se usan como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="b9918-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="b9918-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="b9918-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="b9918-140">[entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="b9918-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="b9918-141">El parámetro _lpszButtonText_ debe ser NULL cuando no es necesario un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="b9918-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="b9918-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9918-142">_ulFlags_</span></span>
  
> <span data-ttu-id="b9918-143">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="b9918-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="b9918-144">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b9918-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="b9918-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b9918-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="b9918-146">Indica que detalles devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, detalles devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="b9918-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="b9918-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b9918-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="b9918-148">Muestra la versión del cuadro de diálogo dirección comunes modal.</span><span class="sxs-lookup"><span data-stu-id="b9918-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="b9918-149">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="b9918-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="b9918-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="b9918-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="b9918-151">Muestra la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="b9918-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="b9918-152">Este marcador es mutuamente excluyente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="b9918-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="b9918-153">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b9918-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="b9918-154">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b9918-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b9918-155">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b9918-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

