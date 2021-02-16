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
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="fc9fb-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="fc9fb-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="fc9fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc9fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc9fb-105">Garantiza que el proveedor de libreta de direcciones de Exchange espera abrir el método **OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="fc9fb-106">Esta función funciona de forma similar a [IAddrBook::D etails](iaddrbook-details.md), pero abre **el entryID** mediante la libreta de direcciones de Exchange identificada por el parámetro _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="fc9fb-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc9fb-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fc9fb-107">Header file:</span></span>  <br/> |<span data-ttu-id="fc9fb-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="fc9fb-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="fc9fb-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fc9fb-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc9fb-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc9fb-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc9fb-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fc9fb-111">Called by:</span></span>  <br/> |<span data-ttu-id="fc9fb-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="fc9fb-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fc9fb-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc9fb-113">Parameters</span></span>

 <span data-ttu-id="fc9fb-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-114">_pmsess_</span></span>
  
> <span data-ttu-id="fc9fb-115">La sesión iniciada **en IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="fc9fb-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="fc9fb-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="fc9fb-118">Puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que usa la función para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="fc9fb-119">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, este parámetro se omite y la función se comporta como [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="fc9fb-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="fc9fb-120">Si este parámetro es NULL o **un MAPIUID** cero, esta función también actúa exactamente igual que [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="fc9fb-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="fc9fb-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="fc9fb-122">[entrada] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="fc9fb-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="fc9fb-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="fc9fb-125">[salida] Identificador de la ventana principal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="fc9fb-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="fc9fb-127">[entrada] Puntero a una función basada en el prototipo **DISMISSMODELESS** o NULL.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="fc9fb-128">Este miembro se aplica solo a la versión no modelada del cuadro de diálogo, como se indica en la DIALOG_SDI marca que se está configurando.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="fc9fb-129">MAPI llama a la función **DISMISSMODELESS** cuando el usuario descarta el cuadro de diálogo de dirección no modelada e informa a un cliente que llama a Details de que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="fc9fb-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="fc9fb-131">[entrada] Puntero a la información de contexto que se pasa a la **función DISMISSMODELESS** a la que apunta el parámetro _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="fc9fb-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="fc9fb-132">Este parámetro solo se aplica a la versión no modelada del cuadro de diálogo incluyendo la marca **DIALOG_SDI** en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="fc9fb-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="fc9fb-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="fc9fb-134">[entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="fc9fb-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fc9fb-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="fc9fb-136">[entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="fc9fb-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="fc9fb-138">[entrada] Puntero a una función basada en el prototipo de **función LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="fc9fb-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="fc9fb-139">Una **función LPFNBUTTON** agrega un botón al cuadro de diálogo de detalles.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="fc9fb-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="fc9fb-141">[entrada] Puntero a datos que se usó como parámetro para la función especificada por el _parámetro lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="fc9fb-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="fc9fb-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="fc9fb-143">[entrada] Puntero a una cadena que contiene texto que se aplicará al botón agregado, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="fc9fb-144">El  _parámetro lpszButtonText_ debe ser NULL cuando no se necesite un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="fc9fb-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc9fb-145">_ulFlags_</span></span>
  
> <span data-ttu-id="fc9fb-146">[entrada] Máscara de bits de marcas que controla el tipo de texto para el _parámetro lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="fc9fb-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="fc9fb-147">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="fc9fb-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="fc9fb-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="fc9fb-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="fc9fb-149">Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="fc9fb-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="fc9fb-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="fc9fb-151">Muestra la versión modal del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="fc9fb-152">Esta marca es mutuamente exclusiva con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="fc9fb-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="fc9fb-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="fc9fb-154">Muestra la versión no modelada del cuadro de diálogo de direcciones comunes.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="fc9fb-155">Esta marca es mutuamente exclusiva con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="fc9fb-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc9fb-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="fc9fb-157">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="fc9fb-158">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="fc9fb-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

