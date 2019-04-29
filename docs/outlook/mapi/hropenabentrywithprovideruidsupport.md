---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409548"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="5c02a-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="5c02a-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="5c02a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c02a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c02a-105">Realiza la misma función que la función [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) , excepto que la función **HrOpenABEntryWithProviderUIDSupport** abre la entrada mediante el objeto support dado en lugar de usar la sesión y la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="5c02a-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c02a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5c02a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c02a-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="5c02a-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="5c02a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5c02a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c02a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c02a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c02a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5c02a-110">Called by:</span></span>  <br/> |<span data-ttu-id="5c02a-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="5c02a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="5c02a-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5c02a-112">Parameters</span></span>

 <span data-ttu-id="5c02a-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="5c02a-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="5c02a-114">a Un puntero a un parámetro _emsabpUID_ que identifica el proveedor de la libreta de direcciones de Exchange que esta función debe usar para mostrar detalles sobre el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5c02a-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="5c02a-115">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, se omite este parámetro y la llamada a la función actúa exactamente como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="5c02a-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="5c02a-116">Si este parámetro es NULL o un MAPIUID de ceros, esta función también actúa exactamente como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="5c02a-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="5c02a-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="5c02a-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="5c02a-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c02a-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="5c02a-119">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5c02a-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5c02a-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c02a-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="5c02a-121">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="5c02a-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="5c02a-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5c02a-122">_lpInterface_</span></span>
  
> <span data-ttu-id="5c02a-123">a Puntero al identificador de interfaz (IID) de la interfaz que se va a usar para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="5c02a-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="5c02a-124">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c02a-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="5c02a-125">Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="5c02a-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="5c02a-126">Para las listas de distribución es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y, para los contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="5c02a-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="5c02a-127">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="5c02a-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="5c02a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c02a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="5c02a-129">a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="5c02a-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="5c02a-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5c02a-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="5c02a-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="5c02a-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="5c02a-132">Indica que los detalles devuelven TRUE si los cambios se realizan realmente en la dirección; de lo contrario, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="5c02a-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="5c02a-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="5c02a-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="5c02a-134">Muestra la versión modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="5c02a-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="5c02a-135">Esta marca se excluye mutuamente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="5c02a-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="5c02a-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="5c02a-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="5c02a-137">Muestra la versión no modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="5c02a-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="5c02a-138">Esta marca se excluye mutuamente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="5c02a-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="5c02a-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c02a-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="5c02a-140">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c02a-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5c02a-141">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5c02a-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5c02a-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="5c02a-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="5c02a-143">contempla Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="5c02a-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="5c02a-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="5c02a-144">_lppUnk_</span></span>
  
> <span data-ttu-id="5c02a-145">contempla Un puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="5c02a-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

