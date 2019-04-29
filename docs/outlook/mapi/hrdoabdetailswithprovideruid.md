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
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="606d2-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="606d2-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="606d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="606d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="606d2-105">Garantiza que el proveedor de libreta de direcciones de Exchange esperado abre el método **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="606d2-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="606d2-106">Esta función funciona de manera similar a [IAddrBook::D etails](iaddrbook-details.md) pero abre **entryID** mediante la libreta de direcciones de Exchange identificada por _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="606d2-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="606d2-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="606d2-107">Header file:</span></span>  <br/> |<span data-ttu-id="606d2-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="606d2-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="606d2-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="606d2-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="606d2-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="606d2-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="606d2-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="606d2-111">Called by:</span></span>  <br/> |<span data-ttu-id="606d2-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="606d2-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="606d2-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="606d2-113">Parameters</span></span>

 <span data-ttu-id="606d2-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="606d2-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="606d2-115">a Un puntero a una _emsabpUID_ que identifica el proveedor de la libreta de direcciones de Exchange esta función debe usarse para mostrar detalles sobre el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="606d2-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="606d2-116">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, se omite este parámetro y la llamada a la función actúa exactamente como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="606d2-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="606d2-117">Si este parámetro es NULL o un MAPIUID de ceros, esta función también actúa exactamente como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="606d2-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="606d2-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="606d2-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="606d2-119">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="606d2-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="606d2-120">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="606d2-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="606d2-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="606d2-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="606d2-122">contempla Identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="606d2-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="606d2-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="606d2-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="606d2-124">a Un puntero a una función basada en el prototipo **DISMISSMODELESS** o null.</span><span class="sxs-lookup"><span data-stu-id="606d2-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="606d2-125">Este miembro sólo se aplica a la versión no modal del cuadro de diálogo, como se indica en la marca DIALOG_SDI que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="606d2-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="606d2-126">MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo Dirección no modal, para informar a un cliente que está llamando detalles que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="606d2-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="606d2-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="606d2-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="606d2-128">a Un puntero a la información de contexto que se va a pasar a la función **DISMISSMODELESS** señalada por el parámetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="606d2-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="606d2-129">Este parámetro solo se aplica a la versión no modal del cuadro de diálogo incluyendo la marca **DIALOG_SDI** en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="606d2-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="606d2-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="606d2-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="606d2-131">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="606d2-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="606d2-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="606d2-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="606d2-133">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="606d2-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="606d2-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="606d2-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="606d2-135">a Un puntero a una función basada en el prototipo de función **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="606d2-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="606d2-136">Una función **LPFNBUTTON** agrega un botón al cuadro de diálogo Detalles.</span><span class="sxs-lookup"><span data-stu-id="606d2-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="606d2-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="606d2-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="606d2-138">a Puntero a los datos que se usaron como parámetro para la función especificada por el parámetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="606d2-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="606d2-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="606d2-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="606d2-140">a Un puntero a una cadena que contiene el texto que se va a aplicar al botón agregado, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="606d2-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="606d2-141">El parámetro _lpszButtonText_ debe ser NULL cuando no es necesario un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="606d2-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="606d2-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="606d2-142">_ulFlags_</span></span>
  
> <span data-ttu-id="606d2-143">a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="606d2-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="606d2-144">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="606d2-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="606d2-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="606d2-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="606d2-146">Indica que los detalles devuelven TRUE si los cambios se realizan realmente en la dirección; de lo contrario, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="606d2-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="606d2-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="606d2-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="606d2-148">Muestra la versión modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="606d2-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="606d2-149">Esta marca se excluye mutuamente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="606d2-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="606d2-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="606d2-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="606d2-151">Muestra la versión no modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="606d2-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="606d2-152">Esta marca se excluye mutuamente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="606d2-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="606d2-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="606d2-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="606d2-154">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="606d2-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="606d2-155">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="606d2-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

