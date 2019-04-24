---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347764"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="27694-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="27694-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="27694-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27694-105">No use esta función.</span><span class="sxs-lookup"><span data-stu-id="27694-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27694-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="27694-106">Header file:</span></span>  <br/> |<span data-ttu-id="27694-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="27694-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="27694-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="27694-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27694-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27694-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27694-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="27694-110">Called by:</span></span>  <br/> |<span data-ttu-id="27694-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="27694-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="27694-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="27694-112">Parameters</span></span>

 <span data-ttu-id="27694-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="27694-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="27694-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="27694-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="27694-115">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="27694-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="27694-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="27694-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="27694-117">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="27694-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="27694-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="27694-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="27694-119">a Puntero al identificador de interfaz (IID) de la interfaz que se va a usar para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="27694-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="27694-120">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="27694-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="27694-121">Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="27694-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="27694-122">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y, para los contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="27694-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="27694-123">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="27694-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="27694-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27694-124">_ulFlags_</span></span>
  
> <span data-ttu-id="27694-125">a Una máscara de máscara de marcadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="27694-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="27694-126">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="27694-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="27694-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="27694-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="27694-128">Indica que los detalles devuelven TRUE si los cambios se realizan realmente en la dirección; de lo contrario, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="27694-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="27694-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="27694-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="27694-130">Muestra la versión modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="27694-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="27694-131">Esta marca se excluye mutuamente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="27694-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="27694-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="27694-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="27694-133">Muestra la versión no modal del cuadro de diálogo Dirección común.</span><span class="sxs-lookup"><span data-stu-id="27694-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="27694-134">Esta marca se excluye mutuamente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="27694-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="27694-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27694-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="27694-136">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="27694-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="27694-137">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="27694-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="27694-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="27694-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="27694-139">contempla Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="27694-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="27694-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="27694-140">_lppUnk_</span></span>
  
> <span data-ttu-id="27694-141">contempla Un puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="27694-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

