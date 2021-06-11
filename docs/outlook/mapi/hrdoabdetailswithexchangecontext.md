---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421371"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="4f08f-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="4f08f-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="4f08f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f08f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f08f-105">Garantiza que el proveedor de la libreta de direcciones espera Exchange abrir el método **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="4f08f-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="4f08f-106">Esta función funciona de forma similar a [IAddrBook::D etails](iaddrbook-details.md), pero abre **el entryID** mediante la libreta de direcciones Exchange identificada por el parámetro _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="4f08f-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f08f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4f08f-107">Header file:</span></span>  <br/> |<span data-ttu-id="4f08f-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="4f08f-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="4f08f-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4f08f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="4f08f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="4f08f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="4f08f-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4f08f-111">Called by:</span></span>  <br/> |<span data-ttu-id="4f08f-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4f08f-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a><span data-ttu-id="4f08f-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="4f08f-113">Parameters</span></span>

 <span data-ttu-id="4f08f-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="4f08f-114">_pmsess_</span></span>
  
> <span data-ttu-id="4f08f-115">La sesión iniciada **en IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="4f08f-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="4f08f-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="4f08f-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4f08f-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="4f08f-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="4f08f-118">Puntero a un **emsmdbUID** que identifica el servicio Exchange que contiene el proveedor de libreta de direcciones de Exchange que usa la función para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4f08f-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="4f08f-119">Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de libreta de direcciones, este parámetro se omite y la función se comporta como [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="4f08f-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="4f08f-120">Si este parámetro es NULL o un **MAPIUID** cero, esta función también actúa exactamente igual que [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="4f08f-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="4f08f-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="4f08f-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="4f08f-122">[in] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4f08f-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="4f08f-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="4f08f-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="4f08f-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4f08f-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="4f08f-125">[salida] Identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f08f-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="4f08f-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="4f08f-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="4f08f-127">[in] Puntero a una función basada en el prototipo **DISMISSMODELESS** o NULL.</span><span class="sxs-lookup"><span data-stu-id="4f08f-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="4f08f-128">Este miembro solo se aplica a la versión modeless del cuadro de diálogo, tal como se indica en la DIALOG_SDI marca que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="4f08f-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="4f08f-129">MAPI llama a **la función DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo dirección de modeless e informa a un cliente que llama a Details de que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="4f08f-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="4f08f-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="4f08f-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="4f08f-131">[in] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el _parámetro lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="4f08f-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="4f08f-132">Este parámetro solo se aplica a la versión modeless del cuadro de diálogo al incluir la marca **DIALOG_SDI** en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4f08f-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4f08f-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f08f-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="4f08f-134">[in] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4f08f-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4f08f-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f08f-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="4f08f-136">[in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="4f08f-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="4f08f-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="4f08f-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="4f08f-138">[in] Puntero a una función basada en el prototipo de función **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="4f08f-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="4f08f-139">Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="4f08f-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="4f08f-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="4f08f-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="4f08f-141">[in] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="4f08f-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="4f08f-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="4f08f-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="4f08f-143">[in] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="4f08f-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="4f08f-144">El  _parámetro lpszButtonText_ debe ser NULL cuando no se necesite un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="4f08f-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="4f08f-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f08f-145">_ulFlags_</span></span>
  
> <span data-ttu-id="4f08f-146">[in] Máscara de bits de marcas que controla el tipo de texto del parámetro _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="4f08f-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="4f08f-147">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="4f08f-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="4f08f-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="4f08f-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="4f08f-149">Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="4f08f-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="4f08f-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="4f08f-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="4f08f-151">Muestra la versión modal del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="4f08f-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="4f08f-152">Esta marca es mutuamente exclusiva con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="4f08f-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="4f08f-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="4f08f-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="4f08f-154">Muestra la versión modeless del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="4f08f-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="4f08f-155">Esta marca es mutuamente exclusiva con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="4f08f-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="4f08f-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4f08f-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="4f08f-157">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f08f-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="4f08f-158">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4f08f-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

