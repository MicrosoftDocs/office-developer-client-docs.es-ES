---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817052"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="58f88-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="58f88-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="58f88-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58f88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58f88-105">Se asegura de que se abre el método **OpenEntry** por el proveedor de la libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="58f88-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="58f88-106">Esta función funciona de manera similar a [IAddrBook::Details](iaddrbook-details.md), pero abre el **entryID** de la libreta de direcciones de Exchange identificado mediante el parámetro _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="58f88-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58f88-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="58f88-107">Header file:</span></span>  <br/> |<span data-ttu-id="58f88-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="58f88-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="58f88-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="58f88-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="58f88-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="58f88-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="58f88-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="58f88-111">Called by:</span></span>  <br/> |<span data-ttu-id="58f88-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="58f88-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="58f88-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58f88-113">Parameters</span></span>

 <span data-ttu-id="58f88-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="58f88-114">_pmsess_</span></span>
  
> <span data-ttu-id="58f88-115">La ha iniciado la sesión **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="58f88-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="58f88-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="58f88-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="58f88-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="58f88-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="58f88-118">Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de la libreta de direcciones de Exchange que se usa la función para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="58f88-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="58f88-119">Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de la libreta de direcciones, se omite este parámetro y la función se comporta como [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="58f88-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="58f88-120">Si este parámetro es NULL o cero **MAPIUID**, esta función también actúa exactamente igual que [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="58f88-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="58f88-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="58f88-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="58f88-122">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="58f88-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="58f88-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="58f88-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="58f88-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="58f88-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="58f88-125">[out] Identificador de la ventana primaria para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="58f88-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="58f88-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="58f88-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="58f88-127">[entrada] Un puntero a una función basándose en el prototipo **DISMISSMODELESS** o NULL.</span><span class="sxs-lookup"><span data-stu-id="58f88-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="58f88-128">Este miembro sólo se aplica a la versión del cuadro de diálogo no modal indicada por el indicador DIALOG_SDI que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="58f88-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="58f88-129">MAPI llama a la función **DISMISSMODELESS** cuando el usuario cierra el cuadro de diálogo no modal de dirección, que le informa de un cliente que llama a detalles que el cuadro de diálogo ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="58f88-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="58f88-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="58f88-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="58f88-131">[entrada] Un puntero a la información de contexto para pasar a la función **DISMISSMODELESS** indicada por el parámetro _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="58f88-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="58f88-132">Este parámetro sólo se aplica a la versión del cuadro de diálogo no modal mediante la inclusión de la marca **DIALOG_SDI** en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="58f88-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="58f88-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="58f88-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="58f88-134">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="58f88-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="58f88-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="58f88-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="58f88-136">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="58f88-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="58f88-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="58f88-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="58f88-138">[entrada] Un puntero a una función según el prototipo de función **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="58f88-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="58f88-139">Una función **LPFNBUTTON** agrega un botón en el cuadro de diálogo detalles.</span><span class="sxs-lookup"><span data-stu-id="58f88-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="58f88-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="58f88-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="58f88-141">[entrada] Un puntero a los datos que se usan como un parámetro para la función especificada por el parámetro _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="58f88-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="58f88-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="58f88-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="58f88-143">[entrada] Un puntero a una cadena que contiene el texto que se aplicará a la se ha agregado un botón, si ese botón es extensible.</span><span class="sxs-lookup"><span data-stu-id="58f88-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="58f88-144">El parámetro _lpszButtonText_ debe ser NULL cuando no es necesario un botón extensible.</span><span class="sxs-lookup"><span data-stu-id="58f88-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="58f88-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58f88-145">_ulFlags_</span></span>
  
> <span data-ttu-id="58f88-146">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="58f88-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="58f88-147">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="58f88-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="58f88-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="58f88-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="58f88-149">Indica que detalles devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, detalles devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="58f88-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="58f88-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="58f88-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="58f88-151">Muestra la versión del cuadro de diálogo dirección comunes modal.</span><span class="sxs-lookup"><span data-stu-id="58f88-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="58f88-152">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="58f88-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="58f88-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="58f88-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="58f88-154">Muestra la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="58f88-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="58f88-155">Este marcador es mutuamente excluyente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="58f88-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="58f88-156">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="58f88-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="58f88-157">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="58f88-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="58f88-158">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="58f88-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

