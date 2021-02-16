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
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="ce698-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="ce698-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="ce698-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce698-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce698-105">Realiza la misma función que la función [HrOpenABEntryWithProviderUID,](hropenabentrywithprovideruid.md) excepto que la función **HrOpenABEntryWithProviderUIDSupport** abre la entrada con el objeto de soporte especificado en lugar de usar la sesión y la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ce698-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce698-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ce698-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce698-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="ce698-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ce698-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ce698-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce698-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce698-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce698-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ce698-110">Called by:</span></span>  <br/> |<span data-ttu-id="ce698-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ce698-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ce698-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce698-112">Parameters</span></span>

 <span data-ttu-id="ce698-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="ce698-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="ce698-114">[entrada] Puntero a un parámetro  _emsabpUID_ que identifica el proveedor de libretas de direcciones de Exchange que esta función debe usar para mostrar detalles sobre el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ce698-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="ce698-115">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="ce698-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="ce698-116">Si este parámetro es NULL o un MAPIUID cero, esta función también actúa exactamente igual que [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="ce698-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="ce698-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="ce698-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="ce698-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ce698-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="ce698-119">[entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ce698-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ce698-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ce698-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="ce698-121">[entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="ce698-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="ce698-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ce698-122">_lpInterface_</span></span>
  
> <span data-ttu-id="ce698-123">[entrada] Puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="ce698-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="ce698-124">Si se pasa NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ce698-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="ce698-125">Para los usuarios de mensajería, la interfaz estándar [es IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="ce698-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="ce698-126">Para las listas de distribución es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y para contenedores es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ce698-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="ce698-127">Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="ce698-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="ce698-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce698-128">_ulFlags_</span></span>
  
> <span data-ttu-id="ce698-129">[entrada] Máscara de bits de marcas que controla el tipo de texto para el _parámetro lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="ce698-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="ce698-130">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="ce698-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="ce698-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ce698-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="ce698-132">Indica que Details devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, Details devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="ce698-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="ce698-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="ce698-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="ce698-134">Muestra la versión modal del cuadro de diálogo dirección común.</span><span class="sxs-lookup"><span data-stu-id="ce698-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="ce698-135">Esta marca es mutuamente exclusiva con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="ce698-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="ce698-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="ce698-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="ce698-137">Muestra la versión modelada del cuadro de diálogo de dirección común.</span><span class="sxs-lookup"><span data-stu-id="ce698-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="ce698-138">Esta marca es mutuamente exclusiva con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="ce698-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="ce698-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ce698-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="ce698-140">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce698-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ce698-141">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce698-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ce698-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="ce698-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="ce698-143">[salida] Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="ce698-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="ce698-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="ce698-144">_lppUnk_</span></span>
  
> <span data-ttu-id="ce698-145">[salida] Puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="ce698-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

