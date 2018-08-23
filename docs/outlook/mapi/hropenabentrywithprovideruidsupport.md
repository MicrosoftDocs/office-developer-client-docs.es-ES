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
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586014"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="75c5c-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="75c5c-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="75c5c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75c5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75c5c-105">Realiza la misma función que la función [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) excepto en que la función **HrOpenABEntryWithProviderUIDSupport** abre la entrada de uso del objeto de soporte determinada en lugar de usar la sesión y la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="75c5c-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75c5c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="75c5c-106">Header file:</span></span>  <br/> |<span data-ttu-id="75c5c-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="75c5c-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="75c5c-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="75c5c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="75c5c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="75c5c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="75c5c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="75c5c-110">Called by:</span></span>  <br/> |<span data-ttu-id="75c5c-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="75c5c-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="75c5c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75c5c-112">Parameters</span></span>

 <span data-ttu-id="75c5c-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="75c5c-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="75c5c-114">[entrada] Un puntero a un parámetro de _emsabpUID_ que identifica el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="75c5c-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="75c5c-115">Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de la libreta de direcciones, este parámetro se omite y el actúa de llamada de función exactamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="75c5c-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="75c5c-116">Si este parámetro es NULL o un cero MAPIUID, esta función también actúa exactamente igual que [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="75c5c-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="75c5c-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="75c5c-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="75c5c-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="75c5c-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="75c5c-119">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="75c5c-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="75c5c-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="75c5c-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="75c5c-121">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="75c5c-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="75c5c-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="75c5c-122">_lpInterface_</span></span>
  
> <span data-ttu-id="75c5c-123">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="75c5c-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="75c5c-124">Pasando NULL, devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="75c5c-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="75c5c-125">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="75c5c-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="75c5c-126">Para las listas de distribución es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y de los contenedores es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="75c5c-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="75c5c-127">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="75c5c-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="75c5c-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75c5c-128">_ulFlags_</span></span>
  
> <span data-ttu-id="75c5c-129">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="75c5c-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="75c5c-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="75c5c-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="75c5c-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="75c5c-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="75c5c-132">Indica que detalles devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, detalles devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="75c5c-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="75c5c-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="75c5c-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="75c5c-134">Muestra la versión del cuadro de diálogo dirección comunes modal.</span><span class="sxs-lookup"><span data-stu-id="75c5c-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="75c5c-135">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="75c5c-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="75c5c-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="75c5c-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="75c5c-137">Muestra la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="75c5c-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="75c5c-138">Este marcador es mutuamente excluyente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="75c5c-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="75c5c-139">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="75c5c-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="75c5c-140">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="75c5c-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="75c5c-141">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="75c5c-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="75c5c-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="75c5c-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="75c5c-143">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="75c5c-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="75c5c-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="75c5c-144">_lppUnk_</span></span>
  
> <span data-ttu-id="75c5c-145">[out] Un puntero a un puntero de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="75c5c-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

