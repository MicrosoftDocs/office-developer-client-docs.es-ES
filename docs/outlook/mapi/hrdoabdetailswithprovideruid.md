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
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426684"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="a1b39-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="a1b39-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="a1b39-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1b39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1b39-105">Garantiza que el proveedor de la libreta de direcciones espera Exchange abrir el método **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="a1b39-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="a1b39-106">Esta función funciona de forma similar a [IAddrBook::D etails,](iaddrbook-details.md) pero abre **entryID** mediante la libreta de direcciones Exchange identificada por _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="a1b39-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b39-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a1b39-107">Header file:</span></span>  <br/> |<span data-ttu-id="a1b39-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a1b39-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a1b39-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a1b39-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1b39-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b39-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1b39-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a1b39-111">Called by:</span></span>  <br/> |<span data-ttu-id="a1b39-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a1b39-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a1b39-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="a1b39-113">Parameters</span></span>

 <span data-ttu-id="a1b39-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="a1b39-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="a1b39-115">[in] Puntero a un _emsabpUID_ que identifica el proveedor Exchange libreta de direcciones que esta función debe usar para mostrar detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a1b39-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a1b39-116">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a1b39-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a1b39-117">Si este parámetro es NULL o un MAPIUID cero, esta función también actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="a1b39-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a1b39-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a1b39-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="a1b39-119">[in] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a1b39-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a1b39-120">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a1b39-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a1b39-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a1b39-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="a1b39-122">[salida] Identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a1b39-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="a1b39-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="a1b39-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="a1b39-124">[in] Puntero a una función basada en el prototipo **DISMISSMODELESS** o NULL.</span><span class="sxs-lookup"><span data-stu-id="a1b39-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="a1b39-125">Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a1b39-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="a1b39-126">MAPI llama a **la función DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a Details de que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="a1b39-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="a1b39-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="a1b39-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="a1b39-128">[in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="a1b39-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="a1b39-129">Este parámetro solo se aplica a la versión modeless del cuadro de diálogo al incluir la marca **DIALOG_SDI** en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a1b39-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a1b39-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1b39-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="a1b39-131">[in] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="a1b39-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a1b39-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1b39-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="a1b39-133">[in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="a1b39-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="a1b39-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="a1b39-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="a1b39-135">[in] Puntero a una función basada en el prototipo de función **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="a1b39-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="a1b39-136">Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="a1b39-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="a1b39-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="a1b39-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="a1b39-138">[in] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="a1b39-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="a1b39-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="a1b39-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="a1b39-140">[in] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="a1b39-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="a1b39-141">El  _parámetro lpszButtonText_ debe ser NULL cuando no se necesite un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="a1b39-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="a1b39-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1b39-142">_ulFlags_</span></span>
  
> <span data-ttu-id="a1b39-143">[in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="a1b39-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="a1b39-144">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="a1b39-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="a1b39-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a1b39-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="a1b39-146">Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="a1b39-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="a1b39-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="a1b39-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="a1b39-148">Muestra la versión modal del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="a1b39-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="a1b39-149">Esta marca es mutuamente exclusiva con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="a1b39-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="a1b39-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="a1b39-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="a1b39-151">Muestra la versión modeless del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="a1b39-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="a1b39-152">Esta marca es mutuamente exclusiva con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="a1b39-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="a1b39-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1b39-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="a1b39-154">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a1b39-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a1b39-155">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a1b39-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

