---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bd42fcd34042c2f9579497f164c4a67f6ba97e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817092"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="6400a-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="6400a-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="6400a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6400a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6400a-105">Realiza la misma función que la función [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) excepto en que la función **HrOpenABEntryWithProviderUIDSupport** abre la entrada de uso del objeto de soporte determinada en lugar de usar la sesión y la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6400a-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6400a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6400a-106">Header file:</span></span>  <br/> |<span data-ttu-id="6400a-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="6400a-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="6400a-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="6400a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6400a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6400a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6400a-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6400a-110">Called by:</span></span>  <br/> |<span data-ttu-id="6400a-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6400a-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6400a-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6400a-112">Parameters</span></span>

 <span data-ttu-id="6400a-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="6400a-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="6400a-114">[entrada] Un puntero a un parámetro de _emsabpUID_ que identifica el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="6400a-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="6400a-115">Si el identificador de entrada entrante no es un identificador de entrada Exchange proveedor de la libreta de direcciones, este parámetro se omite y el actúa de llamada de función exactamente como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="6400a-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="6400a-116">Si este parámetro es NULL o un cero MAPIUID, esta función también actúa exactamente igual que [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="6400a-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="6400a-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="6400a-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="6400a-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6400a-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="6400a-119">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="6400a-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6400a-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6400a-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="6400a-121">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="6400a-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="6400a-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6400a-122">_lpInterface_</span></span>
  
> <span data-ttu-id="6400a-123">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="6400a-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="6400a-124">Pasando NULL, devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="6400a-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="6400a-125">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6400a-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="6400a-126">Para las listas de distribución es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y de los contenedores es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="6400a-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="6400a-127">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="6400a-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="6400a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6400a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="6400a-129">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="6400a-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="6400a-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="6400a-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="6400a-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="6400a-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="6400a-132">Indica que detalles devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, detalles devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="6400a-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="6400a-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="6400a-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="6400a-134">Muestra la versión del cuadro de diálogo dirección comunes modal.</span><span class="sxs-lookup"><span data-stu-id="6400a-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="6400a-135">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="6400a-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="6400a-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="6400a-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="6400a-137">Muestra la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="6400a-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="6400a-138">Este marcador es mutuamente excluyente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="6400a-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="6400a-139">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6400a-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="6400a-140">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6400a-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6400a-141">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6400a-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6400a-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="6400a-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="6400a-143">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="6400a-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="6400a-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="6400a-144">_lppUnk_</span></span>
  
> <span data-ttu-id="6400a-145">[out] Un puntero a un puntero de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="6400a-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

