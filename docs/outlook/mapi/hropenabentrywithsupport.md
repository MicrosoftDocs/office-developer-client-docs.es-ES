---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817083"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="f507b-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f507b-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="f507b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f507b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f507b-105">No use esta función.</span><span class="sxs-lookup"><span data-stu-id="f507b-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f507b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f507b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f507b-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="f507b-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="f507b-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f507b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f507b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f507b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f507b-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f507b-110">Called by:</span></span>  <br/> |<span data-ttu-id="f507b-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f507b-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f507b-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f507b-112">Parameters</span></span>

 <span data-ttu-id="f507b-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="f507b-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="f507b-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f507b-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="f507b-115">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f507b-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f507b-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f507b-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="f507b-117">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="f507b-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="f507b-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f507b-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="f507b-119">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="f507b-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="f507b-120">Pasando NULL, devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="f507b-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="f507b-121">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="f507b-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="f507b-122">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md), y para los contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="f507b-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="f507b-123">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="f507b-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="f507b-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f507b-124">_ulFlags_</span></span>
  
> <span data-ttu-id="f507b-125">[entrada] Una máscara de bits de indicadores que controla el tipo de texto para el parámetro _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="f507b-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="f507b-126">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="f507b-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="f507b-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="f507b-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="f507b-128">Indica que detalles devuelve TRUE si realmente se realizan cambios en la dirección; de lo contrario, detalles devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="f507b-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="f507b-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="f507b-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="f507b-130">Muestra la versión del cuadro de diálogo dirección comunes modal.</span><span class="sxs-lookup"><span data-stu-id="f507b-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="f507b-131">Este marcador es mutuamente excluyente con DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="f507b-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="f507b-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="f507b-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="f507b-133">Muestra la versión del cuadro de diálogo dirección comunes no modal.</span><span class="sxs-lookup"><span data-stu-id="f507b-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="f507b-134">Este marcador es mutuamente excluyente con DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="f507b-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="f507b-135">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f507b-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f507b-136">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f507b-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f507b-137">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f507b-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f507b-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f507b-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="f507b-139">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="f507b-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="f507b-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="f507b-140">_lppUnk_</span></span>
  
> <span data-ttu-id="f507b-141">[out] Un puntero a un puntero de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="f507b-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

